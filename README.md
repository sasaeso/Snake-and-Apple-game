This project is a classic Snake Game with a modern twist, built using HTML5, CSS3, and JavaScript. The game includes dynamic walls, collision effects, and responsive gameplay. Players control the snake, eat apples to gain points, and avoid walls or self-collision.

📝 Features
Dynamic Walls: Walls are generated randomly with each game reset to increase the challenge.
Collision Effects: Visual and shake animations when the snake collides with walls.
Modern Visuals:
Gradient-filled snake body with smooth shapes.
Radial-gradient apples for a polished appearance.
Responsive canvas design for a seamless gameplay experience.
Responsive Gameplay: Arrow keys control the snake, and the game speed remains consistent for smooth interaction.
Score Tracking: Displayed in real-time.
📂 Project Structure
graphql
Copy code
project-folder/
│
├── index.html    # The main HTML file with the game structure.
├── styles.css    # Embedded CSS for the game styling (within the HTML file).
├── script.js     # Embedded JavaScript for game logic (within the HTML file).
🚀 Getting Started
Prerequisites
A modern web browser (Chrome, Firefox, Edge, etc.).
Basic knowledge of HTML, CSS, and JavaScript (optional, for customization).
Steps to Run the Game
Clone or Download the project files.
Open the index.html file in any web browser.
Enjoy the game!
🎮 How to Play
Objective: Control the snake using the arrow keys to eat apples and grow longer.
Rules:
Avoid colliding with walls or yourself.
Apples appear randomly on the canvas; eat them to score points.
The game resets upon collision.
Controls:
Arrow Left (←): Move Left.
Arrow Right (→): Move Right.
Arrow Up (↑): Move Up.
Arrow Down (↓): Move Down.
💻 Code Highlights
Dynamic Walls
Walls are randomly generated using the generateStraightWalls function, ensuring they appear in different locations for every game reset.

javascript
Copy code
function generateStraightWalls() {
  const wallChains = [];
  // Generates random horizontal and vertical wall chains
  ...
  return wallChains.filter(
    wall => wall.x >= 0 && wall.x < canvas.width && wall.y >= 0 && wall.y < canvas.height
  );
}
Collision Effects
The game features a shake animation when the snake collides with a wall.

javascript
Copy code
function animateCollision() {
  if (collisionAnimationFrame < 10) {
    const shakeOffset = collisionAnimationFrame % 2 === 0 ? 5 : -5;
    canvas.style.transform = `translate(${shakeOffset}px, ${shakeOffset}px)`;
    collisionAnimationFrame++;
    requestAnimationFrame(animateCollision);
  } else {
    canvas.style.transform = 'translate(0, 0)';
  }
}
🎨 Styling
Gradient Background: The game has a vibrant gradient background for modern aesthetics.
Apple Design: Uses radial gradients and additional details like stems and leaves for realism.
Snake Design: Gradient-filled, smooth shapes for the snake's body and head.
🤝 Contributing
Feel free to contribute by:

Reporting bugs.
Suggesting new features.
Improving the code or design.
🛠️ Built With
HTML5: For the structure of the game.
CSS3: For styling the game layout and UI.
JavaScript: For game logic and interactivity.
📜 License
This project is licensed under the MIT License. You are free to use, modify, and distribute it as per the terms of the license.

💡 Future Enhancements
Add difficulty levels (easy, medium, hard).
Introduce power-ups or obstacles.
Save high scores using local storage.
👨‍💻 Author
Designed and developed by Mostafa Ashraf.

Enjoy the game and have fun! 🐍🍎
