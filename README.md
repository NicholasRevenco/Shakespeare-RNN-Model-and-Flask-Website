# Shakespeare RNN Model and Flask Website

This project showcases a Shakespeare RNN model and Flask website that illustrates a fascinating intersection between the literary artistry of Shakespeare and the technological prowess of Recurrent Neural Networks (RNNs).

Whether you are an admirer of classic literature or a tech enthusiast intrigued by machine learning, this system is designed to appeal to your curiosity. By utilizing the RNN model provided, you can create text reminiscent of Shakespeare's iconic style, or tailor the system to emulate other authors or even conjure original narratives.

The project is thoughtfully organized into two accessible stages. The first stage focuses on RNN text generation and is demonstrated in the RNNTextGenerationTestModel.ipynb file located in the Website folder. If you wish to delve solely into this engaging world of algorithm-driven literary creation, all the instructions you need are provided there.

For those aspiring to take their exploration a step further, the second stage offers an opportunity to deploy this creativity on a Flask website, facilitated by the FlaskWebsite.ipynb guide. If you choose this path, simply download the repository and place the Website folder in your Google Colabs folder on your Google Drive. Detailed steps for both options are thoughtfully provided below, ensuring a smooth and enjoyable experience for users of all backgrounds.

By bridging the gap between the past and the future, literature and technology, this project invites you to embark on a unique journey that reimagines the timeless magic of storytelling through the lens of artificial intelligence.

### Features:

- Generate text in the style of Shakespeare or other authors
- Create original narratives
- Deploy your text generator on a Flask website
Requirements:
- Python 3
- NumPy
- Pandas
- TensorFlow
- Flask
### How to Use:

To learn more about how to use this project, please see the following guides:

Step 1: RNN Text Generation - RNNTextGenerationTestModel.ipynb

Step 2: Flask Website - FlaskWebsite.ipynb

#


## Step 1: Character-Level Text Generation with RNN - RNNTextGenerationTestModel.ipynb
This project provides a character-level text generation model using a Recurrent Neural Network (RNN) implemented in TensorFlow. It is designed to learn the structure and style of a given text dataset and generate new text snippets accordingly.
If you would like to test the model on the document, download this model (trained on basic epochs and other parameters): <a href="https://www.dropbox.com/scl/fo/wiu3w731jk98wbwspmlco/h?rlkey=pq1brnoh6j65ols73zeygbdxw&dl=0" target="_blank">Model</a>

### Overview:
The code starts with loading a given text dataset and performs preprocessing to create a vocabulary from unique characters. It then prepares sequences of character IDs that are used to build a dataset suitable for training the RNN model.

The RNN model consists of an Embedding layer, a GRU layer, and a Dense layer. The code includes a custom class MyModel to define the architecture, as well as training and evaluation routines using TensorFlow's Keras API.

A special class OneStep is defined to generate text one character at a time, using the trained model. The generation can be controlled with a temperature parameter to adjust randomness.

### Requirements:
Python 3.x
TensorFlow 2.x
NumPy
Google Colab (Optional, if you wish to run the code in Colab environment --- this is how I did it)
### How to Use:
- Load the Data: Specify the path to your text file by modifying path_to_file.
- Preprocess the Text: The code will read the text, create vocabulary, and prepare sequences.
- Define and Train the Model: You can adjust hyperparameters such as embedding_dim, rnn_units, and EPOCHS as needed.
- Generate Text: The code will automatically generate new text snippets using the trained model.
- Save and Load Model: The trained one-step model is saved and can be reloaded for future usage.
### Key Functions:
- split_input_target: Splits sequences into input and target texts.
- MyModel: Custom class defining the RNN architecture.
- OneStep: Class for generating text one step at a time.
### Notes:
- Ensure the specified text file is accessible and properly encoded.
- Experiment with different hyperparameters for varying results.
- If running on Google Colab, the code to mount Google Drive is included.
### Example Output:
After training, the model will print generated text that resembles the style and structure of the original text.

## Step 2: Flask Web Application in Google Colab - FlaskWebsite.ipynb
This repository contains the code for a Flask web application that is designed to run inside Google Colab. The application serves an HTML template and uses a pre-trained TensorFlow model to generate predictions based on user input.

### Getting Started:
The code provided mounts your Google Drive, specifies the directory for HTML templates, and sets up a Flask application. It also uses ngrok to create a secure public URL to your localhost, allowing users to access your Flask application.

### Prerequisites:
- You'll need to have access to Google Colab, and the following packages will be installed within the notebook:
- flask_ngrok
- pyngrok==4.1.1
Installation and Usage:
- Mounting Google Drive: The code mounts Google Drive to access HTML templates and pre-trained models. Make sure your templates and models are available in the specified paths.

- Flask Application Setup: The Flask app is set up with specific routes and renders the HTML templates from a specified folder.

- Predictive Function: A function predict is defined to use a TensorFlow model to generate a sequence of characters as predictions based on the user's input.

- Running the Application: By executing the code, the Flask application will be accessible via a public URL provided by ngrok.

### Code Structure:
The code is divided into several key parts:

- Environment Setup: Installation of necessary packages and authorization with ngrok.

- Application Initialization: Loading HTML templates, creating the Flask app, and running it with ngrok.

- Model Loading: Loading a pre-trained TensorFlow model for generating predictions.

- Prediction Function: A function that takes user input and generates predictions using the loaded model.

- Routes Definition: Definition of the application's routes, handling both GET and POST requests.

- Application Execution: Running the Flask app, making it accessible to the web.

### Important Note:
Make sure to replace the ngrok authtoken with your actual token. You can do this by going to ngrok's website, creating an account, and finding your own token for use. From there, copy it and paste it on the your own doc.
