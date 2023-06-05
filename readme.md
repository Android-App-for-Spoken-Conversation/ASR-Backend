# Flask App

This Flask app utilizes an ASR model and provides two routes: `/` and `/speech`.

## Installation

1. Install Anaconda:
   - Follow the official [Anaconda installation guide](https://docs.anaconda.com/anaconda/install/) to install Anaconda on your system.


2. ASR Setup:
   - Procedure to setup environment for ASR

   - Step 1:conda create -n <name> python=3.7
   - Step 2:conda activate <name>
   - Step 3: git clone https://github.com/Open-Speech-EkStep/vakyansh-wav2vec2-experimentation.git -b ieee
   - Step 4:cd vakyansh-wav2vec2-experimentation
   - Step 5:bash setup_new_env.sh

   If some subprocess error comes run following commands
   - Step 6: cd /opt/wav2vec/kenlm/
   - Step 7: export KENLM_ROOT=$PWD
   - Step 8: cd ../flashlight/bindings/python/
   - Step 9: export USE_CUDA=0
   - Step 10:export USE_MKL=0
   - Step 11:python setup.py install
Download below files:
https://drive.google.com/drive/u/1/folders/1modJVPd4KOcyM-KmP6csGw5y4Mx9iPx6


3. Get the files
    - You can download the files from here 
      ``` 
      https://drive.google.com/drive/folders/1JOwPCh2rLE-ygWb1QygKsNxpYUvLuyun?usp=sharing 
      ```

4. Navigate to the downloaded folder

5. Install dependencies:
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


## Contact
- 20bcs112@iiitdwd.ac.in
- 20bcs048@iiitdwd.ac.in
