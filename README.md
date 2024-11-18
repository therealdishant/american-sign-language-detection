The **Realtime Hand Gesture Recognition System** is an innovative project designed to detect and classify hand gestures in real time using computer vision and machine learning techniques. This system leverages the **MediaPipe** framework, a powerful tool for hand landmark detection, and processes video input captured through a webcam to identify static hand gestures. By analyzing the positions of 21 hand landmarks, the system compares these coordinates against predefined patterns to classify gestures such as "a," "b," and "c" 

The primary objective of this project is to provide an intuitive and non-verbal means of communication with potential applications in **sign language interpretation**, **gesture-based control systems**, and **human-computer interaction**. The system is implemented in **Python** using libraries such as **OpenCV** for real-time video processing and MediaPipe for landmark detection. 

Despite achieving high accuracy and efficiency, the system faces challenges under varying lighting conditions and in distinguishing between complex gestures. Future enhancements could include the recognition of dynamic gestures, integration with IoT devices, and the development of a larger gesture vocabulary. This project highlights the potential of gesture recognition in accessibility, gaming, and AI-driven interfaces, paving the way for more inclusive and interactive technologies.


![332489963-6945d009-8aa7-4bf7-99f8-9743662c5248](https://github.com/user-attachments/assets/90199fb8-abd5-4ffa-b7cd-bc54803ef5b6)





# Table of Contents

1. [Features](#Features)
2. [Requirements](#Requirements)
3. [Installation](#Installation)
4. [Model Training](#Model-Training)
5. [Contributing](#Contributing)


# Features

- **Real-time ASL detection using the device's camera.**
- **Accurate classification of ASL characters using a deep learning model.**
- **Hand landmark tracking for precise gesture recognition.**
- **Support for a wide range of ASL characters and phrases.**
- **High accuracy and robustness in varying lighting conditions.**

# Requirements:

- OpenCV
- MediaPipe
- Pillow
- NumPy
- Pandas
- Seaborn
- Scikit-learn
- Matplotlib
- Tensorflow

> [!IMPORTANT]
> If you face an error during training from the line converting to the tflite model, use TensorFlow v2.16.1.

# Installation:

1. Clone the Repository:

```

```

3. Install Dependencies:

```
pip install -r requirements.txt
```

4. Run the Application:

```
python main.py
```

# Model Training

If you wish to train the model on your dataset, follow these steps:

   ### Data Collection

1. Manual Key Points Data Capturing

Activate the manual key point saving mode by pressing "k", which will be indicated as “MODE: Logging Key Point”.<br>
If you press any uppercase letter from “A” to “Z”, the key points will be recorded and added to the “model/keypoint_classifier/keypoint.csv” file as demonstrated below.

![Screenshot 2024-11-18 170013](https://github.com/user-attachments/assets/560318e3-727e-47b5-b224-9f1440c323eb)



> [!NOTE]
> Each time you press the uppercase letter a single entry point is appended to keypoint.csv.

2. Automated Key Points Data Capturing

Activate the automatic key point saving mode by pressing "d", which will change the content of the camera window to an image of OM606.

> [!NOTE]
> You need to specify the dataset directory in ```app.py```

   ### Training

Launch the Jupyter Notebook "[keypoint_classification.ipynb](keypoint_classification.ipynb)" and run the cells sequentially from the beginning to the end.<br>
If you wish to alter the number of classes in the training data, adjust the value of "NUM_CLASSES = 26" and make sure to update the labels in the "[keypoint_classifier_label.csv](model/keypoint_classifier/keypoint_classifier_label.csv)" file accordingly.
![332244132-0a4c4ce9-4afa-4852-a410-2b9bb280e4b8](https://github.com/user-attachments/assets/b725369c-5676-4feb-ac93-bd7d80556d48)

   ### Model Structure

The following is the image of the model structure that was prepared in the "[keypoint_classification.ipynb](keypoint_classification.ipynb)" notebook.

![332452032-e0940c53-f12b-46da-8526-2ffb9a011634](https://github.com/user-attachments/assets/4b1790ed-4e84-4a81-93ed-bae9aaf7b367)

# Contributing

We welcome contributions to enhance this project! Feel free to use

1. Fork the repository.
2. Create a new branch for your improvements.
3. Make your changes and commit them.
4. Open a pull request to propose your contributions.
5. We'll review your pull request and provide feedback promptly.
