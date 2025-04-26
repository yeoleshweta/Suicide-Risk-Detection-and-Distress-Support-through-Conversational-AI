# Suicide Risk Detection and Distress Support through Conversational AI

Problem
Suicidal ideation and emotional distress are pervasive global mental health issues, yet real-time, emotionally intelligent 
interventions are scarce. Existing NLP systems for suicide detection (e.g., GRU-based classifiers or models used by Shout 
or Reddit datasets) focus solely on classification, often limited to single-turn messages. They neither track multi-turn 
emotional shifts nor offer empathetic, distress-alleviating support in real-time dialogue. There is a critical gap in building 
AI systems that detect risk and actively support individuals in distress through intelligent conversation.

This repository contains two complementary datasets for pilot testing our multi‐modal suicide‐risk and distress‐detection model:

1. **Mental Health Crisis Hotline Logs**  
2. **911 Emergency Call Audio (First 6 Seconds)**

## Contents
## 1. Mental Health Crisis Hotline Logs

- **Source:** Kaggle “Mental Health Crisis Hotline Data” by ptyagi586  
- **Format:** CSV  
- **Files inside `crisis_hotline.zip`:**
  - `hotline_logs.csv`  
- **Fields:**
  | Column         | Type    | Description                                            |
  | -------------- | ------- | ------------------------------------------------------ |
  | `call_id`      | string  | Unique identifier for each call                        |
  | `timestamp`    | string  | ISO 8601 datetime of the call start                    |
  | `issue_type`   | string  | Annotated issue category (e.g. “suicidal thoughts”)     |
  | `duration`     | float   | Call duration in seconds                               |
  | `resolution`   | string  | Outcome tag (“referred”, “resolved”, “escalated”)      |
  | `transcript`   | string  | (Optional) Human‐transcribed text, if available        |

## 2. 911 Emergency Call Audio (First 6 Seconds)

- **Source:** Kaggle “911 Recordings: The First 6 Seconds” by louisteitelbaum  
- **Format:** WAV audio  
- **Directory inside `911_recordings.zip`:**

- **`metadata.csv` fields:**
| Column       | Type    | Description                              |
| ------------ | ------- | ---------------------------------------- |
| `file_name`  | string  | Audio filename (e.g. `0001.wav`)         |
| `location`   | string  | Geographic region of the call            |
| `call_type`  | string  | Category (e.g. “medical”, “fire”, “police”) |

## Usage

1. **Unzip** each archive under `data/raw/`:
 ```bash
 unzip data/raw/text/crisis_hotline.zip   -d data/raw/text/crisis_hotline/
 unzip data/raw/audio/911_recordings.zip  -d data/raw/audio/911_recordings/
