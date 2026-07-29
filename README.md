# <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Hand%20gestures/Waving%20Hand.png" alt="Waving Hand" width="35" height="35" /> Hey There!

**I'm Mert** — a Computer Engineering graduate and M.Sc. student at Marmara University, based in Istanbul, Turkey.

I build AI-powered systems end to end: multi-agent LLM pipelines, real-time perception on point clouds and video, and the production backends that carry them. Lately that means **LangGraph + Gemini** agent orchestration with schema-validated structured outputs, document intelligence over PDFs, and vision pipelines on **PyTorch / YOLO**.

Before the AI side took over, I spent a year shipping enterprise **ASP.NET Core + React** applications at TÜBİTAK UME — architecture, Oracle schema design, and IIS deployment included. That background is still how I think about turning a prototype into something that survives real users.

<img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Light%20Bulb.png" alt="Light Bulb" width="20" height="20" /> Python-first for models and tooling · daily user of AI coding tools with a review- and test-driven workflow · always reading about the next model release.

## <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Hammer%20and%20Wrench.png" alt="Hammer and Wrench" width="30" height="30" /> **Languages and Tools**

**AI / ML & Backend**

[![My Skills](https://skillicons.dev/icons?i=py,pytorch,fastapi,flask,cs,dotnet,postgres,docker&perline=8)](#)

**Frontend & Tooling**

[![My Skills](https://skillicons.dev/icons?i=ts,js,react,next,tailwind,vite,git,github,linux&perline=9)](#)

## <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Travel%20and%20places/Rocket.png" alt="Rocket" width="30" height="30" /> Featured Projects

### <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Travel%20and%20places/Ship.png" alt="Ship" width="22" height="22" /> NavalSight — Real-Time Maritime Target Detection & Tracking
*Graduation project, in collaboration with HAVELSAN · Sept 2025 – June 2026*

> <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Activities/Trophy.png" alt="Trophy" width="16" height="16" /> **2nd place & Achievement Award** among 52 selected projects at Kocaeli University's 4th Graduation Project Exhibition
> <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Activities/Sparkles.png" alt="Sparkles" width="16" height="16" /> **Top 20 of 80** projects — finalist in the HAVELSAN 2025–2026 SUIT-Plus Program

A dual-channel architecture that detects, tracks and classifies three vessel classes (frigate, cargo ship, fast attack craft) from 360° GPU-LiDAR point clouds in real time.

- **Geometric signature channel** — sea-clutter filtering and DBSCAN clustering, then orientation-invariant features: height histograms and a PCA-based Z/X dimension profile.
- **Kinematic trajectory channel** — speed, acceleration, yaw rate and turning radius derived from centroid history. A GRU-based *KalmanNet* (2 layers, ~40K params) trained on AIS data with SmoothL1 + Adam + AMP performs state estimation over noisy trajectories and predicts the next 5 positions from the last 10; a TCN classifies over a 3-second sliding window.
- **Adaptive fusion** — the channels are combined with speed-dependent sigmoidal weights, so geometry dominates for stationary targets and trajectory information takes over for moving ones.

Validated on a hydrodynamically calibrated **Gazebo Harmonic + VRX + ROS 2** simulation across 22 routes and 28,640 LiDAR frames — **85.7–94.6% per-class accuracy** (97–99% for the frigate and cargo classes) at **4.2 ms inference**, guaranteeing real-time operation at 10 Hz.

---

### <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Bar%20Chart.png" alt="Chart" width="22" height="22" /> KOBİ Pilot — Multi-Agent Financial Assistant for SMEs
*BTK Hackathon 2026 · built end to end in 10 days*

A 4-agent **LangGraph** pipeline (data → risk → prioritiser → message) over a shared typed state, orchestrating **Gemini 2.5 Pro/Flash** — reasoning routed to Pro, generation to Flash — with every call returning schema-validated structured JSON (`response_schema` + Pydantic v2).

Document intelligence turns scanned PDF invoices into structured transactions via **pdfplumber + Gemini multimodal**, alongside CSV bank statements. Served from a **FastAPI** backend (async SQLAlchemy, JWT) with a **React + TypeScript** dashboard.

---

### <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Video%20Camera.png" alt="Camera" width="22" height="22" /> Real-Time Shoplifting Detection & Alert System
*Supported by TÜBİTAK 2209-A · Oct 2024 – June 2025*

> <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Activities/Trophy.png" alt="Trophy" width="16" height="16" /> Award-winning at the departmental graduation project exhibition · paper under journal review

Live CCTV streams analysed to flag suspicious behaviour in real time, with alerts routed to security staff over an event-driven **Apache Kafka** framework built for high-throughput video and low-latency delivery.

An **Explainable-AI** module fuses **YOLOv11** object localisation with **GPT-4o** vision calls into automated, human-readable security reports — prompt and tool design tuned to keep frame context within model limits and API cost predictable. The underlying classifier is a voting ensemble of MobileNetV3, ResNet50 and EfficientNetB0 (RNN-augmented): **91.89% accuracy, 0.92 F1**.

## <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Card%20Index%20Dividers.png" alt="Dividers" width="30" height="30" /> More Projects

| Project | What it does | Stack | Links |
| --- | --- | --- | --- |
| **EventGo** | Smart event-planning platform with personalised recommendations, an interactive map, real-time chat, gamification and conflict detection preventing scheduling overlaps | ASP.NET Core, CQRS, SignalR, MS SQL Server, Google Maps API, React, TypeScript, JWT | [Backend](https://github.com/MerttMetinn/EventGoAPI) · [Frontend](https://github.com/MerttMetinn/EventGo-Client) |
| **SmartSync** | Multi-threaded real-time stock & order system — dynamic customer prioritisation and thread synchronisation preventing race conditions on shared stock, with live transaction logging | ASP.NET Core, CQRS, JWT, React, TypeScript, Tailwind, shadcn/ui | [Backend](https://github.com/MerttMetinn/SmartSyncAPI) · [Frontend](https://github.com/MerttMetinn/SmartSync-Client) |
| **Medicasimple Patient Portal** | Patient portal on a .NET 9 microservices backend — independent Auth, Appointment, Registration and Notification services behind an API Gateway handling routing and service-level access control | .NET 9, microservices, API Gateway, React, Vite | [Repo](https://github.com/MerttMetinn/medicasimple-microservices) |
| **CloakDocs** | Blind-review submission workflow with author / editor / reviewer role separation, NER-based anonymisation of sensitive entities and RSA-encrypted data transfer | Python, Flask, PostgreSQL, scispaCy, RSA, Next.js | [Repo](https://github.com/MerttMetinn/CloakDocs) |

## <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Envelope.png" alt="Envelope" width="30" height="30" /> Reach Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/mertmetinn)
[![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mertmetin39@gmail.com)
