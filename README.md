# pygame_skeleton..


provides "scene control" with a global dict:

```
MODE_MAIN = 'MAIN'
MODE_DEFINE_CONTROLS = 'DEFINE_CONTROLS'
MODE_TWO = 'TWO'
GAME_MODE = {}
GAME_MODE['GAME_MODES'] = [MODE_DEFINE_CONTROLS, MODE_MAIN, MODE_TWO]
GAME_MODE['CURRENT_MODE'] = mode['GAME_MODES'][0]
```

a mechanism to define controls based on a dict inside the main_screen class:

```
    controls = [
        {'name': 'up', 'button': None, 'key': None}, 
        {'name': 'down', 'button': None, 'key': None}, 
        {'name': 'left', 'button': None, 'key': None}, 
        {'name': 'right', 'button': None, 'key': None}, 
        {'name': 'fire', 'button': None, 'key': None}    
    ]
```

uses the above game mode dict to provide a dirty little define controls:

```
if GAME_MODE['CURRENT_MODE'] is MODE_DEFINE_CONTROLS:
```

a function to display a quick message in the top left, when your console is covered:

```
self.output(text) 
```
