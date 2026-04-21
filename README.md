# 🧠 FlowOS

AI-powered cognitive optimization for neurodiverse minds.

**Predict your focus. Enter flow on demand.**

FlowOS is an AI-driven system concept designed to help people, especially individuals with ADHD, understand, predict, and optimize their cognitive performance. Unlike traditional productivity tools, FlowOS focuses on cognitive state modeling: transforming daily behavioral data into personalized focus insights and real-time interventions.

This repository currently contains the FlowOS pitch deck as a static HTML presentation.

## 🧑‍💻 Authors

**Aria Shi** [GitHub](https://github.com/AriashininiA), [LinkedIn](www.linkedin.com/in/aria-xingni-shi)
MSE @ Upenn | Machine Learning Engineer | BSc @ UCL | Physics & Math <br>
Focus areas: Model Architecture, AI systems, Reinforcement learning, Applied ML infrastructure

**Shufang Tan** 
Researcher @ Children's Hospital of Philadelphia |
PhD in Cognitive Science |
MSc in Computer Science

## Problem

People with ADHD and other neurodiverse conditions often struggle with:

- Inconsistent focus and energy levels
- Difficulty entering flow state
- Ineffective generic productivity tools
- Limited insight into how habits affect cognition

Existing tools track tasks, but they do not understand your brain.

## Solution

FlowOS builds a personalized AI loop:

```text
Behavior Data -> Pattern Learning -> Focus Prediction -> Actionable Interventions
```

Key capabilities:

- **Behavior tracking:** sleep, nutrition, hydration, activity, and mood
- **Pattern discovery:** identify personal focus triggers and blockers
- **Focus prediction:** estimate optimal cognitive windows throughout the day
- **Flow Mode activation:** provide real-time suggestions to help users enter deep focus

## Core Insight

ADHD is not a discipline problem. It is a state regulation problem.

FlowOS adapts to the user's internal state instead of enforcing rigid routines.

## System Architecture

Planned backend architecture:

```text
app/
├── main.py                         # FastAPI entrypoint
├── schemas.py                      # Pydantic data models
├── routes/
│   ├── analyze.py                  # Behavior -> insights
│   ├── generate.py                 # Recommendations / Flow Mode
│   └── status.py                   # Job tracking
├── services/
│   ├── ingestion_service.py        # Data ingestion: manual + APIs
│   ├── feature_service.py          # Feature engineering
│   ├── modeling_service.py         # Focus prediction models
│   ├── recommendation_service.py   # Intervention logic
│   └── pipeline_service.py         # End-to-end orchestration
└── utils/
    ├── logger.py
    ├── metrics.py
    └── storage.py
```

## Tech Stack

- **Backend:** FastAPI, Python
- **ML/AI:** PyTorch, Transformers, Scikit-learn
- **Data:** SQLite for MVP, scalable database later
- **Infrastructure:** Docker, async job handling
- **APIs:** OpenAI for analysis/reasoning, wearable integrations in future versions

## Modeling Approach

Input signals:

- Sleep duration and quality
- Nutrition signals such as caffeine, sugar, and protein
- Physical activity
- Self-reported focus and mood

Methods:

- Time-series analysis
- Feature engineering with rolling averages and lag features
- Regression/classification models for focus score prediction
- Future reinforcement learning for intervention optimization

## Core Pipeline

1. Collect daily behavioral data
2. Extract features and patterns
3. Predict focus score and focus windows
4. Generate recommendations
5. Collect feedback and improve the model

## MVP Roadmap

**v1: Current**

- Manual logging
- Rule-based insights
- Basic focus estimation
- Static pitch deck

**v2**

- ML-based focus prediction
- Daily recommendations

**v3**

- Real-time adaptive system
- Flow Mode optimization
- Wearable integration

## Use Cases

- ADHD students managing study sessions
- Engineers optimizing deep work time
- Creators improving consistency
- Anyone seeking high-performance cognitive optimization

## Differentiation

| Traditional Apps | FlowOS |
| --- | --- |
| Static schedules | Dynamic adaptation |
| Generic advice | Personalized insights |
| Task tracking | Cognitive state modeling |
| Reminders | Flow-state activation |

## Vision

Build the operating system for neurodiverse cognition.

Future directions:

- Real-time cognitive monitoring
- Cross-user pattern learning
- Integration with wearables such as Apple Watch and EEG devices
- B2B productivity and wellness solutions

## Planned Metrics

- Focus score accuracy
- User retention and engagement
- Intervention success rate
- Recommendation pipeline latency, including p50 and p95

## Why This Project

FlowOS combines:

- ML system design
- Real-world neurodiversity impact
- End-to-end production thinking

It reflects a shift from building models to building intelligent systems that adapt to humans.
