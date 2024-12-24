# Hidden-Markov-Model-from-scratch

## 1. Introduction
Here we train 10 HMM models, one for each digit 0-9. Then we pass our audio into all of these trained models and each model tells us if that audio belogs to that particular group or not. And that's how we recognise our digit

## 2. Dataset

The dataset contains audio files and the naming convention of audio files is `` <digit>_<name_of_person>_<index> ``.

## 3. Visualisation
We have visualised the MFCC features of digits.

Mel-Frequency Cepstral Coefficients (MFCC) are features commonly used in speech and audio processing. They represent the short-term power spectrum of a sound, capturing the phonetically important characteristics of speech. MFCCs are derived by taking the Fourier transform of a windowed signal, mapping the powers of the spectrum to the mel scale, and then taking the discrete cosine transform to obtain a set of coefficients.

In MFCC visualization, the x-axis represents time frames and the y-axis represents the MFCC coefficients (frequency components).

The MFCC features of the same digit seem to follow a similar pattern.

## 4. Models

We have trained 10 different HMM models using ` hmmlearn `. Each model is trained on one digit from 0-9.

We pass the test data into all of these models and for each sample, we check which model out of the 10 models provides the highest likelihood.

## 5. Personal recordings

You can find my recordings in the `dataset/MyRecording/SpojebDigitPersonal`.

The file `0to9.wav` is the file which was created in Audacity and was then parsed into 10 files using the script given in the original `SpokenDigit` Dataset.

## 6. Results

### 6.1 Results on test set

`Test Accuracy: 90.67 (544/600)`

### 6.2 Results on personal data
Unfortunately, I have only 10 personal recordings so the following result is not a correct measure to evaluate our model.
`Test Accuracy: 80.00 (8/10)`