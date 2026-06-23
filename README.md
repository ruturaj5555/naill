# Disease Diagnosis System Using Human Nail Image
Early Stage Disease Diagnosis System Using Human Nail Image Processing Using Deep Learning
💅 Disease Diagnosis System Using Human Nail Image

<sub>by Ruturaj Patil</sub>

An AI-assisted diagnostic tool that analyzes images of human fingernails to detect early visual indicators of underlying health conditions — turning a simple photo into a quick, non-invasive screening aid.


📌 Overview

Fingernails often reveal more about our health than we realize. Doctors have long used nail color, texture, and shape as visual clues during physical examinations — pale nails can hint at anemia, yellowish nails at liver issues or fungal infection, bluish nails at poor oxygen circulation, and spoon-shaped nails at iron deficiency. This project automates that observation process using computer vision and deep learning, allowing a nail image to be analyzed instantly and flagged for potential conditions, rather than relying solely on manual visual inspection.

The system is built as an accessible, low-cost screening tool — not a replacement for professional diagnosis, but a first-line indicator that could prompt someone to seek medical attention sooner.


⚠️ Disclaimer: This project is intended for academic and research purposes only. It is not a certified medical device and should not be used as a substitute for professional medical advice or diagnosis.




✨ Key Features


Image-based disease detection from a single nail photo (captured or uploaded)
Multi-condition classification, trained to recognize indicators of:

Anemia (pale/whitish nail bed)
Jaundice (yellow discoloration)
Cyanosis (bluish tint, linked to low oxygen levels)
Fungal infection (Onychomycosis)
Leukonychia (white spots/patches)
Koilonychia / spoon nails (associated with iron deficiency)
Healthy / Normal nail classification



Image pre-processing pipeline — cropping, normalization, and noise reduction for consistent model input
Confidence score output alongside the predicted condition
Simple web interface for uploading an image and viewing results instantly
Result history log to track previous scans (optional, if persistence is enabled)



🛠️ Tech Stack

LayerTechnologiesModel TrainingPython, TensorFlow / Keras, CNN (Convolutional Neural Network)Image ProcessingOpenCV, NumPy, PillowBackend / APIPython (Flask)FrontendHTML, CSS, JavaScript (or React, depending on implementation)Dataset HandlingPandas, scikit-learn (train/test split, evaluation metrics)

(Swap in your actual stack here if it differs — this reflects the most common approach for this type of project.)


🚀 Getting Started

Prerequisites


Python 3.9+
pip
A trained model file (.h5 or .pkl) — see Model section


1. Clone the repository

bashgit clone https://github.com/<your-username>/disease-diagnosis-nail-image.git
cd disease-diagnosis-nail-image

2. Set up the environment

bashpython -m venv venv

# Activate the virtual environment
venv\Scripts\activate        # Windows
source venv/bin/activate     # macOS / Linux

pip install -r requirements.txt

3. Run the application

bashpython app.py

The app will be available at http://127.0.0.1:5000

4. Use the system


Open the web interface in your browser
Upload a clear, well-lit image of a fingernail
View the predicted condition along with the model's confidence score



🧠 Model Details

DetailDescriptionArchitectureConvolutional Neural Network (custom or transfer learning, e.g. MobileNetV2/ResNet)InputRGB nail image, resized to a fixed input shape (e.g. 224×224)OutputPredicted disease class + confidence percentageTraining DataLabeled nail image dataset, categorized by conditionEvaluation MetricsAccuracy, Precision, Recall, F1-score, Confusion Matrix


📁 Project Structure

disease-diagnosis-nail-image/
├── dataset/
│   ├── train/               # Training images, organized by class
│   └── test/                 # Testing images, organized by class
├── model/
│   ├── train_model.py        # Model training script
│   └── nail_disease_model.h5 # Saved trained model
├── static/                   # CSS, JS, uploaded image storage
├── templates/                # HTML templates for the web interface
├── app.py                    # Flask application & prediction routes
├── requirements.txt          # Python dependencies
└── README.md


📊 Results

MetricScoreTraining Accuracyfill in once trainedValidation Accuracyfill in once trainedTest Accuracyfill in once trained

(Replace with your actual model performance once training is complete.)


🩹 Troubleshooting

Model fails to load


Confirm the trained model file exists in the model/ directory and the filename matches what's referenced in app.py


Low prediction accuracy


Ensure uploaded images are well-lit, in focus, and show the nail clearly without obstruction
Check that the dataset used for training was sufficiently large and balanced across classes


Server not starting


Verify all dependencies in requirements.txt are installed
Check that the correct Python environment is activated



🔭 Future Enhancements


Expand the dataset to cover a wider range of conditions and skin tones for better generalization
Add real-time detection via webcam capture instead of static image upload
Build a mobile app version for on-the-go screening
Integrate explainability tools (e.g. Grad-CAM) to highlight which part of the nail influenced the prediction
Partner with healthcare datasets for more clinically validated training data



🤝 Contributing

This is a learning-focused project, but feedback, bug reports, and pull requests are always welcome. Feel free to open an issue or fork the repo to contribute improvements.


📄 License

This project is intended for educational and research use. Feel free to explore, modify, and build upon it.


🙋 Author

Ruturaj Patil
Built as a college/academic project exploring the intersection of computer vision, deep learning, and accessible health screening tools.
