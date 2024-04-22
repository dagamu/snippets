```python
import pygame

WIDTH = 1280
HEIGHT = 720

class Game:
    def __init__(self, WIDTH, HEIGHT):
        self.window_size = (WIDTH, HEIGHT)
        self.FPS = 60
        self.running = False
    
    def run(self):
        pygame.init()
        self.clock = pygame.time.Clock()
        self.screen = pygame.display.set_mode((WIDTH, HEIGHT))
        
        self.running = True
        while self.running:
            self.loop()
        pygame.quit()
        
    def loop(self):
        self.quit_check()
        self.screen.fill("grey10")
        pygame.display.flip()

        self.clock.tick( self.FPS )
        
    def quit_check(self):
        for e in pygame.event.get():
            if e.type == pygame.QUIT:
                self.running = False

def main():
    game = Game(WIDTH, HEIGHT)
    game.run()
    
if __name__ == "__main__":
    main()
```