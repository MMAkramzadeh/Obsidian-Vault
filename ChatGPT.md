You’ve got a Samsung Galaxy S24 FE. That thing has more horsepower than a mid-range laptop from a few years ago. So performance isn’t the real constraint.
The constraint is architecture.
Hyprland first — reality check
Hyprland is a Wayland compositor. Wayland compositors want:
• Direct GPU access
• DRM (Direct Rendering Manager)
• Kernel graphics interfaces
• Proper display server control
Inside Termux with proot, you don’t get real GPU access. No DRM. No KMS. No systemd session. No logind. You’re sandboxed inside Android’s userspace.
So native Hyprland? Not realistically.
You’d be forcing Wayland to run inside Xwayland inside proot inside Android. That’s turtles stacked on turtles. Performance would be tragic.
Now KDE.
KDE Plasma is technically possible — but heavy. Plasma expects systemd, dbus services, hardware integration. You can make it limp along in proot with VNC, but it won’t feel elegant. It will feel like you duct-taped a spaceship to a skateboard.
What actually works beautifully on phones:
Use an X11 desktop + VNC server.
The sweet spot for “lightweight but pretty”:
• XFCE (stable, light, customizable)
• LXQt (lighter, modern Qt look)
• Openbox + Picom (minimal + compositing effects)
If you want “Hyprland vibes” (tiling, smoothness, minimalism), I’d suggest:
Openbox + Picom + polybar
or
i3 + Picom
That gives you tiling and blur-like effects without Wayland pain.
Here’s the clean setup inside your Arch container:
Inside Arch:
Install Xorg + lightweight desktop:
Copy code

pacman -S xorg-server xorg-xinit tigervnc xfce4 xfce4-goodies
Or for minimalist tiling:
Copy code

pacman -S xorg-server xorg-xinit tigervnc i3 picom polybar
Set up VNC:
Copy code

vncserver
Edit:
Copy code

~/.vnc/xstartup
For XFCE:
Copy code

#!/bin/sh
exec startxfce4 &
For i3:
Copy code

#!/bin/sh
exec i3 &
Make it executable:
Copy code

chmod +x ~/.vnc/xstartup
Then run:
Copy code

vncserver -localhost
On Android, install a VNC viewer and connect to localhost:5901.
You now have a Linux desktop running inside your phone.
Now — performance tuning for smoothness:
• Lower VNC resolution (like 1280x720)
• Use TigerVNC
• Disable heavy compositing effects
• Avoid Plasma unless you accept lag
If you really want modern and beautiful without suffering:
LXQt + Picom
or
XFCE with a good theme + Kvantum
Your S24 FE can handle it. The bottleneck is rendering through VNC, not CPU.
Now here’s the forward-thinking twist.
If you truly want Hyprland-level elegance on a phone, the better route is:
Install a real Linux distro directly on the device (postmarketOS style) — but Samsung bootloaders make that nearly impossible.
Or…
Use your phone as a thin client. Run Arch + Hyprland on a small home server, SSH into it, and forward Wayland/X11. Your phone becomes the portal instead of the host.
That’s philosophically cleaner. Phones are incredible radios. Servers are better desktops.
If you'd like, I can design a “beautiful minimal Arch phone desktop build” optimized specifically for touch interaction — because tiling window managers and thumbs require different ergonomics than keyboards.