# self-color-changing-neural-network-website

This project appears to be a basic HTML, CSS, and JavaScript project, potentially related to machine learning and visual color perception, although some elements suggest a self-driving car context based on the HTML title.

Color Guesser / Self-Driving Car (Concept)
This project explores a simple concept of using a neural network (brain.js) to "guess" whether a randomly generated color should have white or black text on it for optimal readability. While the HTML title refers to "Self Driving Car," the primary functionality observed in the provided code snippets is related to color analysis.

How it Works
The core of this project involves a pre-trained neural network that takes RGB color values as input and outputs a prediction (0 or 1), which is then used to determine if text on that color should be black or white. Users can interact by "training" the network with their own judgments about good color/text combinations.

Project Structure
index.html: The main HTML file providing the structure and UI of the application.

style.css: (Not provided, but would typically contain styling for index.html)

main.js: Contains the JavaScript logic for the neural network, color generation, and UI interactions.

car.js: Contains a Car class, suggesting a potential (but currently unimplemented) connection to a self-driving car simulation.

Features
Neural Network Integration: Utilizes the brain.js library for a simple neural network.

Color Generation: Randomly generates background colors.

Text Color Prediction: The neural network attempts to predict whether white or black text is more suitable for the generated background color.

User Training: Buttons allow users to provide feedback ("White" or "Black") to further train the neural network.

Data Export: A "Print" button logs the training data to the console, which can be used for further analysis or to save trained models.

Basic UI: A simple interface to display colors and text, and interact with the training process.

Technologies Used
HTML5

CSS3 (implied by inline styles in index.html)

JavaScript (ES6+)

brain.js (Neural Network library)

Code Explanation
index.html
Sets up a basic HTML page.

Includes a <style> block for basic CSS, defining a #color div with a black border, centered content, and white class for white text.

The #color div contains "White Text", "Black Text", and a div with id="guess" where the neural network's prediction will display text.

Three buttons: "White", "Black", and "Print" are provided for user interaction.

Links to the brain.js library via a CDN and then to main.js.

car.js
Defines a Car class with a constructor for x, y coordinates, width, and height.

Includes a draw method that uses a 2D rendering context (ctx) to draw a rectangle representing the car.

This file suggests that the project might eventually incorporate a visual simulation, possibly related to self-driving features, but its current connection to the main.js and index.html is not explicitly shown in the provided snippets.

main.js
Neural Network Initialization: const net = new brain.NeuralNetwork(); creates a new neural network instance.

Training Data: const data = [...] contains an array of input (RGB color) and output (1 for white text, 0 for black text) pairs, which are used to train the network. The network is immediately trained with net.train(data);.

DOM Elements: Selects various HTML elements by their IDs (color, guess, white-button, black-button, print-button).

Event Listeners:

"White" button: Calls choseColor(1) when clicked.

"Black" button: Calls choseColor(0) when clicked.

"Print" button: Calls print() when clicked.

setRandomColor():

Generates random r, g, b values for a new color.

Runs the generated color through the neural network (net.run(color)) to get a guess value.

Sets the text color of guessEl to white if guess is greater than 0.5, otherwise black.

Sets the backgroundColor of colorEl to the randomly generated color.

choseColor(value):

Pushes the current color and the value (1 for white, 0 for black) into the data array, effectively adding a new training example.

Calls setRandomColor() to generate a new color.

print(): Logs the entire data array (including any new training data from user interaction) as a JSON string to the console.

Setup and Running the Project
Save index.html, main.js, and car.js in the same directory.

(Optional, but recommended for better styling): Create a style.css file and add custom styles, as the provided index.html uses inline styles that could be moved to a separate file for better organization.

Open index.html in your web browser.
