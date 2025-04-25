# ActiVisor
 A real-time action recognition system for deaf people, translating movements and gestures into visual cues using computer vision to enhance communication and accessibility.
ActiVisor
Real-Time Human Action Recognition System for the Deaf

ActiVisor is a cutting-edge real-time human action recognition system designed specifically for the deaf and hard-of-hearing community. By using advanced computer vision techniques, ActiVisor detects and interprets human actions (such as gestures, body movements, and other non-verbal signals) and converts them into visual cues or alerts. This system provides an intuitive and accessible way for deaf individuals to interact and communicate in both social and professional settings.

Features
Real-time Action Detection: Detects and classifies human actions like gestures, walking, and other movements.

Accessibility Focused: Translates actions into visual cues for the deaf and hard-of-hearing users.

Customizable Alerts: Users can customize how they receive alerts or notifications.

Multi-Purpose Application: Ideal for use in education, social interactions, workplace settings, and more.

Technologies Used
Computer Vision: Using advanced computer vision techniques to detect human actions in real time.

Deep Learning: Employs deep learning models to accurately identify and classify gestures and actions.

OpenCV: For processing images and video feeds in real-time.

TensorFlow/Keras: For building and training deep learning models.

Installation
Clone the repository:

bash
Copy
Edit

Navigate to the project directory:

bash
Copy
Edit
cd ActiVisor
Install required dependencies:

bash
Copy
Edit
pip install -r requirements.txt
Usage
Run the main application:

bash
Copy
Edit
python actiVisor.py
The application will start detecting actions and displaying visual cues based on detected movements.

Customization
Change Alert Settings: Modify the config/settings.json file to customize the visual cues and alerts.

Model Training: If you'd like to train the system on custom actions, follow the instructions in the TRAIN.md file.

Contributing
We welcome contributions! If you have suggestions or improvements, feel free to fork the project and submit a pull request. Please see the CONTRIBUTING.md for more details.
