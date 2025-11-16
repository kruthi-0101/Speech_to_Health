# Speech-to-Health: Dysarthria Detection, Speech Intelligence & Secure Communication System
## Overview:
Speech-to-Health is an intelligent deep-learning system designed to detect dysarthria, transcribe real speech, and analyze communication clarity for clinical and assistive use. It uses a CNN + Transformer model for articulation disorder detection and a Wav2Vec2-based speech recognition module for transcription and speech understanding.

The system was trained and validated on the TORGO Speech Corpus, achieving 99.63% validation accuracy with clinical-grade reliability.

## Key Features:
### 1) Dysarthria Detection:

-> CNN + Transformer model trained on mel-spectrograms of TORGO speech.

-> Classifies audio as Dysarthric or Normal with confidence levels.

-> Outputs severity-level recommendations (Mild / Moderate / Severe).

#### Example Output:

ANALYZING SPEECH: wav_headMic_F03S02_0074.wav

DYSARTHRIA DETECTION:

Status: DYSARTHRIC

Confidence: 1.0000

Recommendation: Intensive speech therapy suggested

### 2) Wav2Vec2 Speech-to-Text Transcription:

Uses Wav2Vec2 (facebook/wav2vec2-base-960h) for accurate transcription.
Optimized for dysarthric and slurred speech.
Automatically reconstructs likely spoken phrases from real audio.

#### Example Transcriptions:

<img width="951" height="383" alt="image" src="https://github.com/user-attachments/assets/742fe19a-01e2-46e5-b73a-1f222b2f35c5" />

### 3) Conversational Speech Understanding:

Recognizes conversational intent from real recordings.

Contexts: Greeting, Medical, Emergency, Daily speech.

Provides context-based recommendations.

#### Examples:

<img width="978" height="278" alt="image" src="https://github.com/user-attachments/assets/3925c4dc-6d8a-401b-b934-3de359af4229" />

### 4) Real Audio Processing:

Processes TORGO .wav files directly.

Computes waveform length, RMS energy, and detection probability.

Achieved 100% prediction accuracy across tested samples.

#### Example Output:

<img width="672" height="264" alt="image" src="https://github.com/user-attachments/assets/3c7dc213-9040-486e-8f0b-90f4c5bee588" />

### 5) Live Scenario Demonstrations:

<img width="970" height="350" alt="image" src="https://github.com/user-attachments/assets/e12b5729-a778-491e-868b-eaa351359686" />

#### Example Output:

Simulated speech: 'Emergency, I need a doctor'

System Response: Emergency intent detected

Action: Medical team alerted, emergency protocol activated.

### 6) Deployment Readiness:

Computes Reliability = Accuracy × Confidence

Grades system (A–C) for deployment readiness.

Generates full report and saves model weights (deployment_ready_system.pth).

#### Example Report:

<img width="561" height="261" alt="image" src="https://github.com/user-attachments/assets/862bdd52-506c-4997-b313-e65d436ee5fb" />

-> Performance Summary:

Dataset: TORGO Speech Corpus (~17,635 audio files)
Training Samples: 10,578
Validation Samples: 3,528
Test Samples: 3,529
Best Validation Accuracy: 99.63%
Precision: 0.9968
Recall: 0.9927
F1 Score: 0.9947
Real Audio Accuracy: 100% (4/4 correct)
Performance Grade: A (Clinical-grade)
Deployment Ready: Yes

-> System Architecture:

<img width="531" height="545" alt="image" src="https://github.com/user-attachments/assets/f303dbb6-bb74-438a-ad12-1e2f4dcab3b1" />

-> Tech Stack:

<img width="840" height="440" alt="image" src="https://github.com/user-attachments/assets/fd57dd3a-e4f8-4e1b-bcd6-63b12b05650d" />

-> Real-World Applications:

Healthcare Automated dysarthria screening and therapy tracking
Assistive Tech Voice-assistive tools for impaired users
Military Stress and articulation analysis in communication
Smart IoT Emergency speech detection at home

-> Project Pipeline:

<img width="891" height="584" alt="image" src="https://github.com/user-attachments/assets/026adc04-9577-44a3-af9d-c9e8e6e25cd2" />

## Conclusion:
The Speech-to-Health system achieved 99.63% accuracy and clinical-grade reliability using the TORGO dataset.
It successfully detects dysarthria, interprets speech, and delivers healthcare-relevant feedback with real-time transcription and analysis.
The model is fully deployment-ready for research and assistive healthcare environments.
