var pos = 0;
let pageWidth = window.innerWidth;
const pacArray = [
  ["PacMan1.png", "PacMan2.png"],
  ["PacMan3.png", "PacMan4.png"],
];
var direction = 0;
var focus = 0;

function Run() {
  let img = document.getElementById("PacMan");
  let imgWidth = img.width;
  focus = (focus + 1) % 2;
  direction = checkPageBounds(direction, imgWidth, pos, pageWidth);
  img.src = pacArray[direction][focus];
  if (direction) {
    pos -= 20;
    img.style.left = pos + "px";
  } else {
    pos += 20;
    img.style.left = pos + "px";
  }
}
setInterval(Run, 100);

function checkPageBounds(direction, imgWidth, pos, pageWidth) {
  if (direction == 0 && pos + imgWidth > pageWidth) direction = 1;
  if (direction == 1 && pos < 0) direction = 0;

  return direction;
}


# Pacman Exercise
This project brings a Pacman image to life using JavaScript, making it move from left to right on the screen while opening and closing its mouth. This was all donw using HTML, CSS and Javascript. We also used the images of Pacman in order to incorporate into our code. 

# Installation
To run this project locally, follow these steps:

Fork this repository or download it to your machine.
Open the project in your preferred code editor.
Run the HTML file in a browser or copy and paste the content of the HTML and JavaScript files into your code editor.
# Usage
Open the HTML file in a web browser to see the Pacman animation. The Pacman image will move horizontally across the screen, simulating movement while its mouth opens and closes.

# Contributing
Contributions are welcome! If you'd like to contribute to this project, feel free to submit a pull request or open an issue.

# License
This project is licensed under the MIT License.
