# ShadowSignals-Environmental-Behavioural-Intelligence-EBINT-Engine
ShadowSignals is a real-time EBINT (Environmental Behavioural Intelligence) system that predicts covert-intent probability using only legal, open-source, non-personal environmental signals.
Runs fully on:

Kaggle Free Tier GPU (P100)

Local-only execution

Zero cloud servers

Zero personal data

100% Open OSINT sources

Core Features
1️⃣ Live Multi-Camera Fallback System

Uses multiple public webcams (Windy, worldcams, or Insecam extractors)

If one camera fails, switches automatically to the next

Ensures uninterrupted real-time EBINT data

2️⃣ Real-Time Signal Extraction

Extracts 20+ environmental micro-signals:

Traffic density

Crowd-flow optical flow

Night-light intensity

Weather (Open-Meteo or OpenWeatherMap)

Public trend spikes (Google Trends)

Public transport delays (GTFS)

Region activity baseline (from OSM)

Image entropy & movement energy

3️⃣ ShadowSignal Vector (SSV)

A fixed-length normalized vector used for ML:

Traffic + Crowd + Night + Weather + Trends + Entropy + Baseline Shifts + Diversity Weights

4️⃣ Deep Autoencoder (GPU)

Heavy PyTorch model

Trained online

Computes anomaly score

Detects unusual environmental patterns

5️⃣ ShadowGraph Fusion Engine

Fuses:

Anomaly score

Entropy changes

Baseline shifts

Diversity weights

Multi-signal confirmation

Produces a raw covert-intent score.

6️⃣ ShadowScore (0–100)

Final probability after:

Nonlinear scaling

Weather correction

Baseline offsetting

Smoothing

7️⃣ Real-Time Dashboard + Log Feed

Shows:

Timestamp

ShadowScore

All signal values

Baseline shifts

Last 5 cycles

Auto-refresh every 5 minutes

⭐ System Architecture
Live Webcam Frame → EBINT Extractors → ShadowSignal Vector → GPU Autoencoder
→ Anomaly Score → ShadowGraph → ShadowScore → Dashboard/Logs

⭐ Dynamic / Real-Time Capabilities

✔ Live webcam frames every cycle
✔ Weather refreshed every cycle
✔ Trends fetched dynamically
✔ GTFS if available
✔ Baselines recomputed
✔ Autoencoder online training
✔ Auto-loop 24/7 in Kaggle

✅ 2. FUNCTIONALITY SUMMARY
✔ Multi-Camera Fallback

Prevents system failure due to offline cameras.

✔ Entropy-Based Behavioural Modelling

Detects abnormalities in scene activity.

✔ Autoencoder Anomaly Detection

GPU-powered unusual pattern detection.

✔ Environmental Micro-Signal Fusion

Combines 20+ signals legally & safely.

✔ Noise Correction

Weather + holidays + regional baseline shift.

✔ ShadowGraph Correlation Layer

Weighted correlation model for covert-intent probability estimation.

✔ ShadowScore

Scaled 0–100 final output.
