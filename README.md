# Breakout Game

A classic arcade-style Breakout game built with pure JavaScript and DOM manipulation, deployed on GitHub Pages.

🎮 **Play the game:** [https://middlesea.github.io](https://middlesea.github.io)

## Project Overview

This is a browser-based Breakout game developed as part of the grit:lab curriculum. The game features:

- **Pure JavaScript implementation** - No frameworks or canvas, just DOM manipulation
- **60 FPS performance** - Smooth gameplay using optimized rendering techniques
- **Progressive difficulty** - Ball speed increases with each level
- **Classic arcade aesthetics** - Retro green CRT-style visuals
- **Full game mechanics** - Lives system, scoring, timer, and multiple levels

## How to Play

- **Arrow Keys (Left/Right)**: Move the paddle
- **Spacebar**: Start the game
- **P**: Pause/Resume
- **R**: Restart (from pause menu)

Destroy all bricks by bouncing the ball off your paddle. Different colored bricks award different points:
- Red bricks (top): 7 points
- Orange bricks: 5 points
- Green bricks: 3 points
- Yellow bricks (bottom): 1 point

## Project Structure

```shell
MiddSea.github.io/
├── index.html          # Main game page
├── game.js             # Game logic and mechanics
├── style.css           # Game styling
├── docs/               # Documentation
│   ├── README.md       # Game documentation
│   ├── game_design.md  # Design decisions
│   ├── technical.md    # Technical details
│   └── learning.md     # Development journal
├── experiments/        # Development experiments
└── util/              # Deployment utilities
```

## Local Development

1. Clone the repository:
   ```bash
   git clone https://github.com/MiddSea/MiddSea.github.io.git
   cd MiddSea.github.io
   ```

2. Open `index.html` in a modern web browser, or use a local server:
   ```bash
   python3 -m http.server 8080
   # Then visit http://localhost:8080
   ```

## Deployment

This repository is configured for automatic deployment to GitHub Pages:

- The `main` branch is automatically deployed to https://middlesea.github.io
- Changes pushed to `main` are live immediately
- No build process required - pure static HTML/CSS/JS

## Technical Highlights

- **MVC Architecture** - Clean separation of game logic, rendering, and state
- **DOM-based rendering** - No canvas, pure CSS transforms for 60 FPS
- **Compositor optimization** - Uses `translateZ(0)` for hardware acceleration
- **Collision detection** - Precise ball-brick and ball-paddle physics
- **Game state management** - Handles start, pause, game over, and level progression

## Version

Current version: **v0.4.0** - Feature complete with 60 FPS performance across all game states

## Author

Sean Middleton (@smiddleto)

## License

This project is part of the grit:lab curriculum.
