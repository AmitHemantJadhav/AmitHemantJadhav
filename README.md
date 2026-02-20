<div align="center">

<img src="https://capsule-render.vercel.app/api?type=rect&color=0d1117&height=1&section=header" width="100%" />

```
 █████╗ ███╗   ███╗██╗████████╗         ██╗ █████╗ ██████╗ ██╗  ██╗ █████╗ ██╗   ██╗
██╔══██╗████╗ ████║██║╚══██╔══╝         ██║██╔══██╗██╔══██╗██║  ██║██╔══██╗██║   ██║
███████║██╔████╔██║██║   ██║            ██║███████║██║  ██║███████║███████║██║   ██║
██╔══██║██║╚██╔╝██║██║   ██║       ██   ██║██╔══██║██║  ██║██╔══██║██╔══██║╚██╗ ██╔╝
██║  ██║██║ ╚═╝ ██║██║   ██║       ╚█████╔╝██║  ██║██████╔╝██║  ██║██║  ██║ ╚████╔╝ 
╚═╝  ╚═╝╚═╝     ╚═╝╚═╝   ╚═╝        ╚════╝ ╚═╝  ╚═╝╚═════╝ ╚═╝  ╚═╝╚═╝  ╚═╝  ╚═══╝ 
```

**Builder. ML Engineer. Founder.**

West Lafayette, IN | CS & Mathematics (Honors) at Purdue University | Class of 2027
Concentration in Machine Learning & Software Engineering

[![LinkedIn](https://img.shields.io/badge/LinkedIn-amithjadhav-000?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/amithjadhav)
[![GitHub](https://img.shields.io/badge/GitHub-AmitHemantJadhav-000?style=flat-square&logo=github&logoColor=white)](https://github.com/AmitHemantJadhav)
[![Email](https://img.shields.io/badge/Email-jadhah01@pfw.edu-000?style=flat-square&logo=gmail&logoColor=white)](mailto:jadhah01@pfw.edu)

</div>

---

### About

I work across the full stack and then some — frontend to backend, ML pipelines to robotics, serverless infrastructure to published research. I'm as comfortable fine-tuning a YOLO model as I am designing an event-driven backend or programming a lunar rover.

Currently the **Software & Autonomous Systems Lead for NASA Lunabotics** at PFW (our university's first-ever team), **ML Team Lead at BASF through Purdue DataMine**, and the **Founder of Prepify** — a voice-first AI interview platform headed to Y Combinator.

Before this, I spent a summer at **CCTech** building production ML pipelines that replaced weeks of manual engineering work with sub-200ms inference calls. I hold a **patent for a hydrogen-based diya design**, have won **$1,000+ in hackathon prizes**, and speak four languages.

---

### Experience

**Machine Learning Intern — Centre for Computational Technologies (CCTech)**
`May 2024 – Aug 2024`

Designed and deployed an end-to-end **Floorplan Detection System** that converts architectural PDFs into structured CAD-ready geometry — eliminating ~60% of manual drafting time across the pipeline.

Built the full ML stack: fine-tuned **YOLOv9** for element detection (+20% accuracy), developed OCR pipelines with **Tesseract** for tabular/image-heavy documents (+15% extraction accuracy), and integrated **OpenCV** for geometric preprocessing. Deployed as serverless inference on **AWS Lambda + API Gateway + S3**, sustaining p50 ~200ms / p95 <350ms at 100+ concurrent requests. Hardened the system with input validation, circuit-breaker retries, and dead-letter queues — zero data-loss incidents post-launch. CloudWatch-driven tuning reduced infrastructure costs by 15%.

`Python` `OpenCV` `YOLOv9` `Tesseract` `AWS Lambda` `API Gateway` `S3` `CloudWatch`

---

### What I'm Building

<table>
<tr>
<td width="50%" valign="top">

#### Prepify

**Voice-first AI interview platform — B2C + B2B**

Prepify conducts real, adaptive voice interviews powered by **Vapi + Gemini**, then generates comprehensive performance reports with multi-modal analysis.

The system fine-tunes **Whisper** and **NVIDIA Canary** models to analyze speech patterns — pace, filler words, clarity, confidence. A separate video analysis pipeline scores body language and eye contact. Questions are dynamically generated from your resume, job description, role, and experience level using advanced prompt engineering with **Gemini 2.0 Flash**.

The backend is a fault-tolerant event-driven architecture on **AWS (Lambda, API Gateway, S3, SQS)** with **Neon PostgreSQL + Drizzle ORM**, featuring idempotent jobs, rate limiting, retries, structured logging, and crash-safe session state. The platform handles 200+ concurrent sessions at p95 <250ms round-trip audio latency.

The B2B platform lets companies create standardized interview kits with rubric-based evaluation, send single-use candidate links, and compare candidates at scale — replacing the first round of human interviews entirely.

Currently applying to **Y Combinator**.

`Next.js 15` `TypeScript` `Vapi` `Gemini` `Whisper` `NVIDIA Canary` `AWS Lambda` `SQS` `S3` `Neon PostgreSQL` `Drizzle ORM` `Clerk` `Stripe`

</td>
<td width="50%" valign="top">

#### NASA Lunabotics

**Autonomous lunar excavation rover — Software & Systems Lead**

I lead the entire software stack for **PFW's first-ever NASA Lunabotics team** — building a rover that autonomously navigates, excavates, and constructs berms on a simulated lunar surface. The competition scores heavily on autonomy (600 points for full autonomous operation), and every collision with a rock or crater costs 30 points. Perception isn't optional — it's the difference between winning and losing.

**Perception stack:** LiDAR point cloud processing for crater detection using elevation grid analysis and depression thresholding. Rock detection through 3D clustering with **YOLOv9** depth fusion as a secondary pipeline. All perception outputs publish as ROS2 topics (`OccupancyGrid`, `PointCloud2`) that feed directly into Nav2's costmap layers.

**Navigation:** Full **ROS2 Humble + Nav2 + BehaviorTree.CPP** autonomy stack running on a **Jetson Orin Nano**. Path planning with obstacle inflation, GPS-denied localization, and multi-cycle autonomous operation.

**Telemetry & Control:** Real-time telemetry dashboard, driver fallback systems, and hardware integration across embedded controllers.

The team includes four software leads (AI/Perception, Navigation, Telemetry, Firmware) plus mechanical and systems engineers. I coordinate the full software architecture and integration across all subsystems.

**Competition: May 2026 at Kennedy Space Center.**

`Python` `ROS2 Humble` `Nav2` `BehaviorTree.CPP` `OpenCV` `Open3D` `YOLOv9` `Jetson Orin Nano` `LiDAR`

</td>
</tr>

<tr>
<td width="50%" valign="top">

#### PFW Shuttle App

**Real-time campus transit tracking system**

PFW had no shuttle tracking system — students had no idea where the shuttle was or when it would arrive. We built the solution from scratch.

The driver app broadcasts GPS pings over **Ably** WebSockets. The backend processes these in real-time, computing ETAs using distance-to-stop, average shuttle speed, and route geometry through a background worker that runs continuous calculation cycles. Students see live shuttle positions on a map with arrival predictions, route selection, and stop lists.

Built with anti-spoofing GPS validation, driver shift management, and a UI designed to match the quality bar of Apple Maps and Uber — not a college side project.

`React Native (Expo)` `TypeScript` `Node.js` `Express` `MongoDB` `Ably` `Clerk` `Google Maps API`

</td>
<td width="50%" valign="top">

#### [CodeSense](https://github.com/AmitHemantJadhav/CodeSense)

**AI-powered codebase intelligence**

A semantic code search and Q&A engine that actually understands your repository. Handles 500K+ lines of code across 10K+ file monorepos using **AST-aware chunking** — not naive text splitting — combined with **LangChain**, **OpenAI embeddings**, and a hybrid retrieval engine (Pinecone vector index + PostgreSQL metadata).

Features incremental indexing via GitHub webhooks, query caching, multi-turn conversational debugging, and cross-conversation memory powered by **AssemblyAI** for meeting transcription and retrieval. Responses deep-link to the exact file and line.

Deployed on a **T3 stack** (Next.js, Prisma, PostgreSQL, AWS Lambda) with Clerk OAuth, Stripe credit-based monetization, and CI/CD via GitHub Actions. Median query latency ~180ms, p95 <400ms, 99.9% uptime.

`TypeScript` `Next.js` `LangChain` `Pinecone` `OpenAI` `Prisma` `PostgreSQL` `AWS Lambda` `AssemblyAI` `Stripe`

</td>
</tr>

<tr>
<td width="50%" valign="top">

#### [BackStory](https://github.com/AmitHemantJadhav/backstory-v2)

**Voice-first storytelling tool for founders**

Most founders can't articulate their origin story clearly. BackStory fixes that through guided voice conversations that extract, structure, and refine raw narratives into compelling pitches.

Built with **Vapi SDK** for real-time voice streaming/transcription and **Gemini** for dynamic narrative generation with emotional tone modeling. The prompt engine features rolling memory, intent detection, and adaptive follow-up logic — maintaining context across 30-minute sessions with p95 <300ms latency.

Includes crash-safe session resume, transcript checkpointing, backpressure handling, structured observability (logs/metrics/traces), and CI/CD with automated testing.

Built for the **Vapi Build Challenge 2025**.

`JavaScript` `Vapi SDK` `Gemini` `React` `TypeScript` `Tailwind CSS` `ShadCN UI`

</td>
<td width="50%" valign="top">

#### [OpenCV MCP Server](https://github.com/AmitHemantJadhav/opencv-mcp)

**Computer vision capabilities for AI agents**

An MCP (Model Context Protocol) server that gives AI assistants like Claude and GPT access to real **OpenCV** computer vision operations — edge detection, thresholding, contour analysis, object detection, and tracking.

Instead of AI models describing what they'd do with an image, they can actually process it. The server exposes OpenCV's full image and video processing pipeline through MCP's standardized tool interface, making computer vision a plug-and-play capability for any MCP-compatible AI system.

`JavaScript` `OpenCV` `Model Context Protocol`

</td>
</tr>

<tr>
<td width="50%" valign="top">

#### RecallOS

**Multi-agent AI audio memory system**

Most transcription tools analyze one recording at a time. RecallOS analyzes patterns *across* all your conversations — tracking speaker engagement evolution, topic timelines, decision patterns, and cross-conversation insights that no single transcript could reveal.

Built as a multi-agent system on **Google Cloud Run** with 7 integrated GCP services: Cloud Storage, Firestore, Gemini 2.0 Flash, Google Embeddings API, Cloud Logging, and more. Each agent handles a specific domain (transcription, embedding, pattern detection, insight synthesis) and coordinates through an orchestration layer.

Built for the **Google Cloud Run Hackathon**.

`Python` `Google Cloud Run` `Gemini` `Firestore` `Embeddings API` `Cloud Storage`

</td>
<td width="50%" valign="top">

#### Collaborative Code Editor

**Real-time multi-user editing with conflict resolution**

A Google Docs-style code editor supporting simultaneous multi-user editing with zero conflicts. Implemented **CRDTs** (Conflict-free Replicated Data Types) for mathematically guaranteed consistency and **WebSocket** connections for real-time synchronization across all connected users.

Features syntax highlighting for multiple programming languages, user session management, and autosave via **AWS Lambda** with low-latency backups to **DynamoDB**.

Deployed with **Kubernetes** and **Docker** for horizontal scalability and fault tolerance under high concurrent traffic.

`Next.js` `WebSockets` `CRDTs` `Node.js` `AWS Lambda` `Kubernetes` `Docker` `DynamoDB`

</td>
</tr>

<tr>
<td colspan="2" valign="top">

#### RT-DETRv2 — Enhanced Object Detection for Autonomous Vehicles

**Research Symposium Presentation**

Optimized a transformer-based real-time detection architecture (RT-DETRv2) for autonomous driving scenarios. Fine-tuned on the **BDD100K** dataset with augmentation strategies, achieving **2.7% higher mAP** and **7.8% improvement in critical object detection** (pedestrians, cyclists, small vehicles) while maintaining **88 FPS** inference speed.

Built a distributed training pipeline using **AWS EC2** (P4d instances), **NVIDIA DALI** for GPU-accelerated data loading, **PyTorch** with mixed precision training, and experiment tracking via **Weights & Biases**. The work demonstrated that targeted fine-tuning of transformer detectors can meaningfully improve safety-critical detection without sacrificing real-time performance.

`PyTorch` `RT-DETRv2` `NVIDIA DALI` `BDD100K` `AWS EC2` `Weights & Biases` `Docker` `CUDA` `DVC`

</td>
</tr>
</table>

---

### Tech

```
Languages        Python, TypeScript, JavaScript, C, C++, Java, SQL
ML / CV          PyTorch, TensorFlow, OpenCV, YOLOv9, Whisper, LangChain, Scikit-learn
LLMs / AI        Gemini, OpenAI, Vapi, RAG pipelines, Vector Embeddings, Prompt Engineering
Frontend         React, Next.js 15, Tailwind CSS, ShadCN UI, React Native (Expo)
Backend          Node.js, Express, tRPC, Drizzle ORM, Prisma, WebSockets
Databases        PostgreSQL, MongoDB, Redis, Firebase, Pinecone, DynamoDB
Cloud            AWS (Lambda, S3, SQS, EC2, API Gateway, CloudWatch), GCP (Cloud Run, Firestore)
Robotics         ROS2, Nav2, BehaviorTree.CPP, Open3D, LiDAR, Jetson Orin Nano
DevOps           Docker, Kubernetes, GitHub Actions, CI/CD, Serverless Architecture
Tools            Git, Figma, Postman, Stripe, Clerk, Weights & Biases
```

---

### Highlights

```
Patent Holder                 Hydrogen-based Diya (lamp) — issued patent for sustainable design
Hackathon Champion            $1,000+ in prizes across Google GenAI, AWS Barrier Breakers, and more
Case Competition Champion     1st place among 20+ teams — Purdue Fort Wayne, Fall 2023
NASA Lunabotics Lead          Building PFW's first-ever competition entry for Kennedy Space Center 2026
Y Combinator Applicant        Prepify — voice-first AI interview platform
ML Team Lead @ BASF           Leading supervised ML initiatives through Purdue DataMine
Languages                     English, Hindi, Marathi, German
```

---

<div align="center">

*"The people who are crazy enough to think they can change the world are the ones who do."* — Steve Jobs

[![LinkedIn](https://img.shields.io/badge/Let's_connect-000?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/amithjadhav)

</div>
