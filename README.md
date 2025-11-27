# ShadowSignals-Environmental-Behavioural-Intelligence-EBINT-Engine
ShadowSignals is a real-time EBINT (Environmental Behavioural Intelligence) system that predicts covert-intent probability using only legal, open-source, non-personal environmental signals.
Runs fully on:

Kaggle Free Tier GPU (P100)

Local-only execution

Zero cloud servers

Zero personal data

100% Open OSINT sources

ShadowSignals — Real-Time EBINT Intelligence Engine
Zero Personal Data • 100% Legal OSINT • Real-Time Environmental Behaviour Analysis

ShadowSignals is a next-generation Environmental Behavioural Intelligence (EBINT) system that predicts covert-intent probability using only open-source, real-world environmental micro-signals.

It provides a ShadowScore (0–100) that represents the intensity of unusual behaviour in any region using:

Public webcam snapshots

Weather & atmospheric patterns

Crowd movement via optical flow

Traffic density via pixel congestion

Trend anomalies (Google Trends)

Transport disruptions

Night-light fluctuations

Entropy-based uncertainty modelling

Autoencoder anomaly detection (P100 GPU accelerated)

OSM region baseline modelling

Multi-camera fallback system

5-minute real-time update cycle

The entire system runs end-to-end inside a Kaggle Notebook with zero cost and zero infrastructure.

 Features
✅ Live OSINT Environmental Signals

Public webcams (snapshot URLs)

Multi-camera fallback with automatic switch-over

Real-time weather (Open-Meteo)

Real-time crowd flow via optical flow

Night-light intensity analysis

Traffic density estimation

Google Trends dynamic anomaly

Transport delays (GTFS, if available)

Entropy of each modality

✅ AI Signal Fusion (ShadowGraph Engine)

Diversity-weighted fusion

5-minute rolling smoothing

Weather & holiday correction

Per-region dynamic baselines via OSMnx

Entropy-weighted anomaly adjustments

Autoencoder anomaly score injection

Final ShadowScore (0–100)

✅ Deep Autoencoder (GPU Accelerated)

Heavy encoder–decoder architecture

Latent bottleneck for anomaly scoring

Continuous online learning buffer

Adaptive training

✅ Real-Time Dashboard

Top signal display

Real-time ShadowScore

Baseline shift visualization

Log feed of last 100 cycles

Cycle timing & system status

Real-Time Workflow

Fetch webcam snapshot

Extract traffic, crowd-flow, night-light

Ingest weather + trends + transport

Build ShadowSignal vector

Compute autoencoder anomaly score

Fuse signals using ShadowGraph

Generate ShadowScore (0–100)

Log + dashboard + next cycle

Loop refreshes every 5 minutes.

Installation (Kaggle)

No installation needed — just open a Kaggle Notebook and run:

!pip install pytube yt-dlp opencv-python-headless pytrends requests aiohttp nest_asyncio tqdm \
           scikit-learn torch torchvision torchaudio folium osmnx shapely \
           geopy gtfs-realtime-bindings numpy pandas matplotlib

Usage
Start the auto-loop
await shadowsignals_auto_loop(
    webcam_url=LIVE_WEBCAM_URL,
    youtube_url=None,
    gtfs_url=None,
    interval=300   # 5 minutes
)

Live multi-camera fallback (optional)

Just list them:

WEBCAM_LIST = [
    "URL1",
    "URL2",
    "URL3"
]


ShadowSignals will automatically switch to the next camera when one fails.

Privacy & Ethics

ShadowSignals processes:

No faces

No license plates

No humans individually

No PII

Only legal public OSINT

Only environmental signals

This system is for research, safety, anomaly spotting, and environmental threat modelling — not surveillance.

Why Environmental Intelligence (EBINT)?

Because human intent influences their environmental impact, even without identifying individuals.

ShadowSignals observes:

Density shifts

Light anomalies

Flow irregularities

Weather disruptions

Public-pattern divergence

Not people.

Outputs
Example Dashboard:
Timestamp: 2025-11-27 17:12:46 UTC  
ShadowScore: 100 / 100  

Top Signals:
- traffic_density: 0.0000
- crowd_flow: 0.0000
- night_light: 0.0000
...
- entropy_trend: 1.8280
- weighted_trend: 119.600

Contributing

PRs are welcome!
You may add:
New EBINT signals
Better fusion algorithms
LSTM + Autoencoder hybrid
Regional multi-point baselines
Visualization dashboards

License
MIT License (recommended)

Credits
Developed by: Asmit Dam
Powered on: Kaggle P100 GPU Free Tier
Data sources: OSINT-only (public webcams, weather, trends, GTFS)

Final Message

ShadowSignals is a fully dynamic, real-time, zero-cost intelligence system — one of the first open-source EBINT engines built to run entirely on Kaggle.
