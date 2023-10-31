# Friend or Foe Identifier

The "Friend or Foe Identifier" is a Python-based program that captures faces from a live webcam feed, trains image datasets with corresponding IDs, and then recognizes faces in real-time. Unidentified faces are indicated as "enemies."

## Algorithm Overview

### Face Detection
This program uses the OpenCV library to perform face detection. It uses a prebuilt frontal face training model (Cascade Classifier) for face detection, often referred to as a Haar Cascade. The Cascade Classifier can identify faces in images and is the basis for our face detection process.

### Face Recognition
For face recognition, this program employs the Local Binary Patterns Histograms (LBPH) algorithm. The LBPH algorithm extracts local binary patterns from face images and builds histograms to represent the unique features of each person's face. It is a simple yet effective method for face recognition.

### Training the Recognizer
The `train.py` script collects a dataset of face images, converts them to grayscale, and detects faces within these images using the Cascade Classifier. It then associates each detected face with a unique ID. The ID is based on the filename of the image in the dataset.

The LBPH Face Recognizer is trained with these grayscale face images and their corresponding IDs. The trained model is saved into a file named `trainer.yml`.

## Usage
1. Run the `gen.py` script to capture face images from a live webcam feed. The images are stored in the "dataset" directory with filenames that serve as the IDs.

2. Use the `train.py` script to train the face recognizer with the collected face images and IDs. The trained model is saved in the "trainer" directory as `trainer.yml`.

3. Run the `rec.py` script to recognize faces in real-time using the trained model. Unidentified faces are considered "enemies."

## Dependencies
The program relies on the following Python libraries:
- OpenCV (cv2)
- NumPy
- Python Image Library (PIL)

Ensure that you have these libraries installed in your Python environment.

## License
This program is provided for educational and research purposes. You are encouraged to use and modify it for your specific needs. However, please consider licensing and attribution if you plan to use it for commercial or public purposes.

**USE RESPONSIBLY**.

## Author @ raam96
This program was authored by the project owner.

Feel free to contact the author for any inquiries or additional information npraam@hotmail.com.

For detailed information on the code logic and implementation, please refer to the code comments in the respective Python files.

Happy face recognition!
