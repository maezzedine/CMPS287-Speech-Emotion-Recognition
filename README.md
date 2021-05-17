# Speech Emotion Recognition

## Emotions Detected: 
  - ANGRY 
  - DISGUST
  - FEAR 
  - HAPPY 
  - NEUTRAL
  - SAD 
  - SURPRISE

## Datasets:
- [RAVDESS](https://www.kaggle.com/uwrfkaggler/ravdess-emotional-speech-audio): 
  + 1440 files
  + 24 actors: 2 females and 2 males
  
- [CREMA-D](https://www.kaggle.com/ejlok1/cremad):
  + 7,442 files
  + 91 actor: 43 females and 48 males
 
- [SAVEE](https://www.kaggle.com/ejlok1/surrey-audiovisual-expressed-emotion-savee):
  + 480 files
  + 4 male actors
  
- [TESS](https://www.kaggle.com/ejlok1/toronto-emotional-speech-set-tess):
  + 2800 files
  + 2 actresses
  
## Data Augmentation:
We augmented our data in order to increase its size. We used the following methods: add_noise, stretch, shift, pitch, speed_up, slow_down, all using LIBROSA. This increased our data 7x.

## Feature Extraction:
We used LIBROSA to calcuate the MFCC of the audio files. This technique is used in similar tasks where it helps in analysing audio.

## Model Specification:
- Classic sequential neural network with 4 hidden layers having 256, 128, 64, and 32 neurons respectively. 
- Each of the layers uses the ReLU activation function and is followed by a dropout layer with a rate of 0.1. 
- The output layer has 7 neurons and uses a softmax activation function since we are performing multiclass classification. 
- The total number of trainable parameters is 58,567.
 
## Results
- Out-of-sample accuracy: 89.55%
- Out-of-sample loss: 0.32

![Learning Curve](https://raw.githubusercontent.com/maezzedine/CMPS287-Speech-Emotion-Recognition/master/media/learning_curve.png?token=AKPLNOLUKM4UPP5Y5EULMP3AVPUR2)
![Loss Curve](https://raw.githubusercontent.com/maezzedine/CMPS287-Speech-Emotion-Recognition/master/media/loss_curve.png?token=AKPLNOPKUZLZIKA6QKZKVFTAVPU3W)
