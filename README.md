# BUBBLE_SHOOTING_GAME
What the Game Does 
This is a basic Bubble Shooter game made using Pygame, where a player shoots colored bubbles from a cannon at the bottom. When three or more same-colored bubbles connect, they pop.

🧩 Code Explanation in Key Sections
1. Imports and Initialization
import pygame, random, math
→ Imports game library, randomness for bubble colors, and math for angle calculations.

pygame.init()
→ Starts all Pygame modules.

Sets up the screen size, font, and game clock.

2. Color Setup
Defines RGB values for colors like RED, GREEN, BLUE, etc., for drawing bubbles and the cannon.

3. Classes
a. Bubble Class
Represents each bubble in the game.

__init__: Sets the bubble's position, color, and radius.

draw(screen): Draws the bubble on screen.

move(angle): Updates position based on shooting angle (used for the bubble being fired).

collides(other): Checks if it hits another bubble.

b. Cannon Class
Controls the shooting cannon.

__init__: Sets cannon’s angle and shooting position.

draw(screen): Draws the cannon as a line.

rotate_left() / rotate_right(): Adjusts cannon angle.

shoot(color): Creates a new Bubble and shoots it in current direction.

4. Functions
a. create_grid(rows, cols)
Creates a grid of bubbles with random colors to start the game.

b. draw_grid(screen, grid)
Draws all the bubbles in the grid.

c. check_collision(moving_bubble, grid)
Checks if the fired bubble collides with any on the grid.

d. find_cluster(grid, x, y, color, visited)
Finds all connected bubbles of the same color (for popping).

e. remove_cluster(grid, cluster)
Removes the popped bubbles from the grid.

f. snap_to_grid(grid, bubble)
Snaps the bubble to the nearest grid location after collision.

5. Main Game Loop
Runs continuously until the user quits.

Fills screen with black.

Handles user input:

Arrow keys rotate the cannon.

Spacebar fires a bubble.

Moves and draws the fired bubble.

Checks for collisions and pops bubbles if needed.

Updates the display with pygame.display.flip().

6. Exit
On quit, it exits the Pygame window and stops the game.

🎮 Controls Summary
← / → Arrow Keys: Rotate the cannon left or right.

Spacebar: Fire the current bubble.
