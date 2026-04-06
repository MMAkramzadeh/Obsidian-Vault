
```python
import pygame
from sys import exit
pygame.init()

running = 1
width = 1920
height = 1200
screen = pygame.display.set_mode(width, height)
Clock = pygame.timer.Clock()
pygame.display.set_caption("Game Name")

while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = 0
            exit()
            
    pygame.display.update()
    clock.tick(60) #Caps the Max Framerate to 60fps
```