# Flask App

This Flask app utilizes an ASR model and provides two routes: `/` and `/speech`.

## Installation

1. Install Anaconda:
   - Follow the official [Anaconda installation guide](https://docs.anaconda.com/anaconda/install/) to install Anaconda on your system.

2. Create a virtual environment (recommended):
   - Open a terminal or Anaconda Prompt, navigate to the project directory, and run the following command to create a new virtual environment named "flask_env":
     ```
     conda create -n flask_env python=3.9
     ```

3. Activate the virtual environment:
   - Run the following command to activate the virtual environment:
     ```
     conda activate flask_env
     ```

4. Get the files
    - You can download the files from here 
      ``` 
      https://drive.google.com/drive/folders/1JOwPCh2rLE-ygWb1QygKsNxpYUvLuyun?usp=sharing 
      ```

5. Navigate to the downloaded folder

6. Install dependencies:
   - Run the following command to install the required dependencies from the `requirements.txt` file:
     ```
     pip install -r requirements.txt
     ```

## Usage

1. Run the server:
   - Execute the following command to start the Flask server:
     ```
     python app.py
     ```

2. Access the routes:
   - `/`:
     - This route supports both GET and POST requests.
     - It allows you to upload a file from the web interface.
   - `/speech`:
     - This route accepts POST requests.
     - It expects an audio file (received from Firebase) as input.
     - It returns a JSON response containing the Hindi text-to-speech result.

## File Structure

- `app.py`: The main Flask application file.
- `single_file_inheritence.py`: An intermediate file that connects the Flask server with the ASR model.
- `requirements.txt`: A list of Python dependencies required by the Flask app.
- `lm.binary` : Language model file
- `lexicon.lst`: Lexicon file
- `dict.ltr.txt`: Letter dictionary file containing unicodes of hindi alphabets
- `final_model.pt`: ASR model file
- `static/`: Folder containing static assets which let you run app on web(CSS, JavaScript, images, etc.)
- `templates/` # Folder containing HTML templates


##Contact
20bcs112@iiitdwd.ac.in
20bcs048@iiitdwd.ac.in
