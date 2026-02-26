# TS-JEPA-on-Time-Series-Anomaly-Prediction.ipynb

***I toyed with this work with the slight conviction that it might double down as my M.Tech Dissertation. But at the point of writing this, I had not decided about that.***

## 1. Hypothesis
To demonstrate the effectiveness of TS-JEPA's Non-Generative Modelling on Industrial Time-Series Anomaly Detection problems.

## 2. Methodology
I employed a Time-Series Joint-Embedding Predictive Architecture (TS-JEPA). This approach utilized Self-Supervised training on data from *Normal* scenarios, followed by evaluation on *Mixed* and *Attack* scenarios.

## 3. Architecture
I used the typical TS-JEPA architecture, consisting of the following main components:
- *1DCNN Tokenizer*
- *Encoder:* Processes the non-masked patches.
- *Predictor:* Generates the target predictions from the encoder’s output.
- *EMA-Encoder:* Encodes the target masked patches.
- *VICReg Loss function:* Regularizer to prevent latent collapse
_Note: The Encoders and Predictor all utilizes a Transformer Backbone._

## 4. Dataset
I used the *Secure Water Treatment (SWaT) Dataset* in this work.

[Kaggle Link:](https://www.kaggle.com/datasets/vishala28/swat-dataset-secure-water-treatment-system/data)

*Nature:* Text-based, tabular time-series data.

*Scale:* Approximately 1.4 million second-by-second data points.

## 5. Results
_Initial prototyping showed promise, with the following key findings:_

*VUS-PR Score:* _0.8763_

*F1-Score:* _0.9807_

*Explanability analysis* indicates that the model is effectively identifying points of anomalies and their likely causes.

