# JS_game_pacman

1. The layout squares is displayed in layout.txt. Width * height = 28 * 28 = total of 782 squares.

2. Definded each square with a digit:
  // 0 - pac-dots
  // 1 - wall
  // 2 - ghost-lair
  // 3 - power-pellet
  // 4 - empty

3. Used setInterval() and clearInterval() to defind the movement of the ghosts: bliky, pinky, inky and clyde.

4. Used addEventListener("keyup") to control the pacman.
Calculation is as following:
* down - 
if (pacmanCurrentIndex = NOT contain "ghost-lair" && NOT contain "wall" && pacmanCurrentIndex + width < width * width)
then pacmanCurrentIndex += 28
* up - 
if (pacmanCurrentIndex = NOT contain "ghost-lair" && NOT contain "wall" && pacmanCurrentIndex - width > 0)
then pacmanCurrentIndex -= 28
* left - 
if (pacmanCurrentIndex = NOT contain "ghost-lair" && NOT contain "wall" && pacmanCurrentIndex % width != 0)
then pacmanCurrentIndex -= 1;
      if (pacmanCurrentIndex === 364) {
        pacmanCurrentIndex = 391;
      }
* right - 
if (pacmanCurrentIndex = NOT contain "ghost-lair" && NOT contain "wall" && pacmanCurrentIndex % width < width - 1)
then pacmanCurrentIndex += 1;
      if (pacmanCurrentIndex === 391) {
        pacmanCurrentIndex = 364;
      }

5. When pacman eats the pellets, scores will count up. IF a powerPellet is eaten, change the ghost colors and speed for 10 sec then back to normal style of each ghost automatically.

6. Define game over and win
