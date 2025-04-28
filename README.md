# Check point 2: Suicide Risk Detection and Distress Support Project - Dataset README
Team Members: Yateen Sudhir Sakhare and Shweta Sharma

## Overview
This project aims to build a Conversational AI system capable of detecting suicide risk and distress levels while providing appropriate emotional support. For this, we have curated and organized datasets from multiple reliable sources that collectively cover suicide risk detection and emotional understanding.

This README documents:
- The source of each dataset
- Why the dataset was chosen
- What each dataset file and field represents
- Any limitations, assumptions, or special considerations

---

## Dataset Sources and Purpose

### 1. Crisis Hotline Logs Dataset
- **Source**: Internal document (real-world crisis hotline data)
- **Purpose**: Core dataset to model suicide risk detection and crisis conversations.
- **Contents**:
  - `call_id`: Unique identifier for each call.
  - `timestamp`: Time of the call.
  - `issue_type`: Type of crisis (suicidal, anxious, etc.).
  - `duration`: Duration of call.
  - `resolution`: How the call was resolved.
  - `transcript`: Available for some calls (optional field).

### 2. GoEmotions Dataset
- **Source**: Kaggle Dataset by Debarshi Chanda ([Link](https://www.kaggle.com/datasets/debarshichanda/goemotions))
- **Purpose**: Distress and emotion classification (e.g., sadness, fear) for emotional support modeling.
- **Contents**:
  - `text`: Reddit comment expressing emotions.
  - `labels`: One or multiple emotions (joy, sadness, anger, fear, etc.).

### 3. 911 Call Recordings Dataset (Optional - Future Scope)
- **Source**: Kaggle Dataset by louisteitelbaum
- **Purpose**: Auxiliary dataset for future extension into multimodal (audio-text) emotion detection.
- **Contents**:
  - `wav` audio files: First 6 seconds of emergency calls.
  - `metadata.csv`: Metadata containing location, type of call (medical/fire/police).

> **Note**: This dataset is auxiliary and will not be part of the primary text-based evaluation for this checkpoint.

---

## Why These Datasets Were Chosen
- **Crisis Hotline Logs** provide real-world crisis dialogue structure needed for suicide risk modeling.
- **GoEmotions Dataset** offers nuanced emotional labeling, enhancing emotional intelligence capabilities to better detect distress and support users.
- **911 Call Recordings** offer authentic audio cues for potential future work on detecting distress from voice tone.

This combined dataset strategy ensures the project addresses both suicide risk and emotional distress detection comprehensively.

---

## Folder Structure
```plaintext
suicide_risk_detection_dataset/
├── raw_data/
│   ├── crisis_hotline_logs.csv
│   ├── goemotions_dataset.csv
│   ├── 911_calls_audio/ (optional)
│       ├── *.wav (audio files)
│       └── 911_metadata.csv
├── processed_data/
│   ├── cleaned_crisis_logs.jsonl
│   ├── cleaned_goemotions.jsonl
├── README.md
└── LICENSE (optional)
```

---

## Limitations and Assumptions
- **Annotation Subjectivity**: Suicide risk and emotional sentiment labeling involve human judgment and may contain some noise.
- **Single-Turn Limitations**: Some datasets are single-turn and may require multi-turn conversation simulation for modeling.
- **911 Audio Data**: Audio-only, not included in primary text-based training for this checkpoint.
- **Class Imbalance**: Certain emotions and crisis types might be underrepresented; balancing techniques will be used during training.

---

## Compliance with Project Checkpoint Requirements
- **Authenticity**: Datasets are sourced from real-world crisis text logs and authentic emotional conversations.
- **Diversity**: Multiple datasets cover suicide risk and emotional support aspects.
- **Clear Documentation**: Each dataset's source, purpose, fields, and limitations have been described.
- **Feasibility**: The datasets are manageable in size for a 10-week project timeline and sufficient to build a working prototype.

Thus, this dataset setup is fully compliant with the guidelines provided for Checkpoint 2.

---

## Acknowledgements
We thank the dataset creators and annotators for their contributions to the research community.

