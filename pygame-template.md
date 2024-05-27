```python
import pygame

WIDTH: int = 1280
HEIGHT: int = 720

WINDOW_POS: tuple[int, int] = (1015, 30)
os.environ['SDL_VIDEO_WINDOW_POS'] = '%i,%i' % WINDOW_POS

class Game:

    FPS: int = 60
    running: bool = False

    def __init__(self, WIDTH, HEIGHT):
        self.window_size = (WIDTH, HEIGHT)
    
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
