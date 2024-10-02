Face Recognition App
Overview
This project is a Face Recognition Application developed using Python. It allows users to load images or use their camera to detect and recognize faces. The application integrates multiple machine learning models trained using PyTorch, Keras, and uses a pickle file for managing new person data.
Features:
- Load images from the system.
- Detect faces using OpenCV’s Haar Cascade classifier.
- Recognize faces using:
   - PyTorch .pt model.
   - Keras .h5 model.
   - A pickle model for additional person data.
- If a face is not recognized, the user can input the person’s name and retrain the Keras model.
- Save and update face recognition data dynamically.
Installation
To run this project, you need to install the following dependencies:
1. Clone the repository or download the project files.

2. Create a Python virtual environment (optional but recommended):

python -m venv env
source env/bin/activate  # On Windows use: env\Scripts\activate

3. Install the required libraries:

pip install -r requirements.txt

Required Libraries:
- opencv-python
- PyQt5
- torch
- tensorflow
- numpy
- pickle

Example:
pip install opencv-python PyQt5 torch tensorflow numpy
Usage
Running the Application:
1. Ensure the trained models are placed in the same directory as the script:
- your_model.pt (PyTorch model)
- your_model.h5 (Keras model)
- your_model.pkl (Pickle model)

2. Run the application:
python face_recognition_app.py

3. The UI will open with the following options:
- Load Image: Load a face image from your system.
- Open Camera: Activate your camera to detect and recognize faces.
- Close Camera: Stop the camera feed.
- Exit: Close the application.

4. If a face is not recognized, the user can add the person’s name, retrain the Keras model, and update the pickle file.
File Structure

├── face_recognition_app.py    # Main application file
├── your_model.pt              # Pre-trained PyTorch model
├── your_model.h5              # Pre-trained Keras model
├── your_model.pkl             # Pickle file for person names
└── README.md                  # Project documentation

Model Training and Updates
The application allows users to update the recognition model in real-time:
- When a new person is detected, the user can input the person’s name.
- The Keras model and the pickle file are updated to include the new person’s data.
- The updated Keras model is saved to your_model.h5, and the pickle file is saved as your_model.pkl.
Notes:
Ensure your system's webcam is accessible if you plan to use the camera feature.
The application will automatically resize face images to fit the model input size (e.g., 224x224 for Keras).
For better performance, it’s recommended to use well-trained models that are optimized for face recognition tasks.
License
This project is open-source and free to use. Feel free to modify or improve it according to your needs.
About Author
Name: Eng.Ahmad Ali Abduh Muhammad.
Email: alghlanyahmedali@gmail.com.
