# Audio Emotion Detection App 🎵

This Android application detects emotions from uploaded audio files using a **TensorFlow Lite** model trained on the **RAVDESS dataset**.

## Features ✨
### Upload Voice:
- Users can select and upload an audio file from their mobile device.
- The app analyzes the audio using TensorFlow Lite and predicts the corresponding emotion along with the prediction's accuracy.

### Supported Emotions:
- Neutral  
- Happy  
- Sad  
- Angry  
- Fearful  
- Surprised  

## Dataset 📂
The **RAVDESS dataset** is used to train the TensorFlow Lite model.  
[RAVDESS Dataset Link](https://drive.google.com/drive/folders/1be4CdN_1_GQerHqo6NbrQHwbZ-LkcEFc?usp=sharing)

---

## Model Used 🧠
- **TensorFlow Lite model** for efficient on-device inference.
- Various models were evaluated (CNN-BiLSTM, GRU, MLP, GNN).
- **GRU model** performed best with an **accuracy of 88%**, and thus, it is used in this application.

### Model Performance Summary:
- **Best Accuracy**: GRU with **88%**  
- **Fastest Training**: MLP  
- For detailed comparisons, refer to the [model comparison summary](./model_comparison_summary.txt).

---

## Prerequisites 🛠️
- **Android Studio** (latest version)  
- **Kotlin programming language**  
- **Android SDK** with API Level 24+  
- TensorFlow Lite dependencies

---

## How to Run the App 🚀

1. **Clone this repository**:
   ```bash
   git clone https://github.com/your-username/audio-emotion-detection.git
   cd audio-emotion-detection
2. Open the project in Android Studio.

3. Download the TensorFlow Lite model and place it in the assets directory

4. Ensure the build.gradle file contains
aaptOptions {
    noCompress "tflite"
}


5. Sync the project with Gradle.

6. Build and run the app on a connected Android device or emulator.

## Dependencies 📦
In the build gradle:
dependencies {
    implementation 'org.tensorflow:tensorflow-lite:2.12.0'
    implementation 'org.tensorflow:tensorflow-lite-support:0.4.3'
    implementation 'androidx.core:core-ktx:1.10.1'
    implementation 'androidx.appcompat:appcompat:1.6.1'
    implementation 'com.google.android.material:material:1.9.0'
}


## App Workflow 🛠️
1. Upload Audio: User selects an audio file from their device.
2. Analyze Emotion: The app uses the TensorFlow Lite model to predict the emotion from the audio file.
3. Display Result: The detected emotion and accuracy are displayed on the screen.

##Script for Mobile App Video 🎥
As part of the Mobile Application Development course at Amrita School of Computing, we developed AudiEmotion: Audio Emotion Detection, an app focused on emotion detection through speech/audio analysis. The app is designed to assist within the Accessibility & Assistive Technology domain, specifically in Affective Computing and Audio Emotion Recognition.

Our project utilizes the RAVDESS dataset to train several deep learning models, including CNN, GRU, an Improved CNN-BiLSTM Hybrid Model, MLP, and GNN. Testing revealed that CNN achieved an accuracy of 94.4%, while the Improved CNN-BiLSTM Hybrid Model provided the highest accuracy at 95%. ResNet followed closely at 96%, with the GRU at 88%, MLP at 93%, MobileNetV2 at 82.4%, and GNN at 84.5%.

The dataset can be accessed here: [RAVDESS Dataset Link](https://drive.google.com/drive/folders/1be4CdN_1_GQerHqo6NbrQHwbZ-LkcEFc?usp=sharing)

For a demonstration of the app in action, [Demo Link](https://drive.google.com/file/d/1x0AEPdn9t5uH9WWaLCSOaEO0SOdRRI7u/view?usp=sharing).

The complete source code for EmotiSense is open-source and available on GitHub: [GitHub Link](https://github.com/Aadithya-04/Audio_Emotion_Detection.git)

## Acknowledgments 🙏
1. RAVDESS Dataset for providing the labeled audio samples.
2. TensorFlow Lite for on-device inference.
