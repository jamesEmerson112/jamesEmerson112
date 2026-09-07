# Hi there! I'm James Emerson Vo (An Thien Vo)

I train and evaluate language models under tight compute budgets and analyze GPU execution down to SASS. I am a graduate computer science student at Georgia Tech OMSCS, based in San Francisco.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square)](https://www.linkedin.com/in/james-vo/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/jamesEmerson112)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=flat-square&logo=googlechrome&logoColor=white)](https://jamesemerson112.github.io)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:james.emerson.vo.2503@gmail.com)

## Now

- I submitted a 1.0805 BPB three-seed result to OpenAI's Parameter Golf challenge as pull request #2005, which is open and unmerged, and the full project write-up lives in [DL-Team-Proposal](https://github.com/jamesEmerson112/DL-Team-Proposal).
- I keep a running study repository of AI and GPU papers with my own notes at [James-neural-network-study](https://github.com/jamesEmerson112/James-neural-network-study), most recently adding interactive search and graph visualizations for CS 6601 Artificial Intelligence.
- I am building [SF-city](https://github.com/jamesEmerson112/SF-city), a Godot and Python simulation of San Francisco where synthetic residents commute between imported real streets and buildings, with optional Rust helpers accelerating selected operations.

## Featured work

### ML training and evaluation

- **[DL-Team-Proposal](https://github.com/jamesEmerson112/DL-Team-Proposal)** is the CS 7643 team project that trained a language model to fit inside a 16 MB compressed artifact on 8xH100 GPUs with PyTorch, reaching 1.0805 BPB against an official naive baseline of 1.2244.
- **[AI-CDS-Disease-Diagnosis-Reproduction-Alpha](https://github.com/jamesEmerson112/AI-CDS-Disease-Diagnosis-Reproduction-Alpha)** reproduces a 2022 IEEE Access clinical decision support paper, fixing a patient-level data leakage bug and matching the 21 GB BioSentVec baseline on every retrieval metric with a 416 MB Bio_ClinicalBERT encoder.
- **[MongoDB-Agentic-context-window](https://github.com/jamesEmerson112/MongoDB-Agentic-context-window)** benchmarks OpenAI models on the BABILong needle-in-a-haystack task across context lengths, where gpt-4.1 held 91% accuracy at 64k context against 87.5% for gpt-4o-mini while costing about 40 times more.

### Georgia Tech coursework

- **[backprop-by-hand](https://github.com/jamesEmerson112/backprop-by-hand)** is the public notes and experiments companion to my private CS 7643 coursework, covering hand-derived backward passes from a two-layer MLP through Transformers and DDPMs, and reporting 97.8% MNIST test accuracy. No assignment solution code is included.
- **[gpu-showcase](https://github.com/jamesEmerson112/gpu-showcase)** turns two CS 8803 GPU projects into public animations, including a SASS branch-divergence analyzer that flagged 136 divergent branches across 20 compiled CUDA kernels. The tensor-core simulator extension matched the course reference exactly but ran slower on every half-precision benchmark. Live: [animations](https://jamesemerson112.github.io/gpu-showcase/)
- **[Robotic-AI-A-start-Search-and-Drone-SLAM](https://github.com/jamesEmerson112/Robotic-AI-A-start-Search-and-Drone-SLAM)** is a write-up and demo-GIF showcase of three Artificial Intelligence for Robotics projects, covering particle-filter spaceship localization, online-graph SLAM for a drone, and A\* pathfinding. The source stays private under the Georgia Tech honor code.

### Hackathons

- **[WeddingAI](https://github.com/jamesEmerson112/WeddingAI)** is a solo Stanford x DeepMind hackathon submission that turns a phone video of an empty wedding venue into a Gemini-designed theme and builds toward a 3D Gaussian-splat reconstruction of the room. Running the reconstruction by hand on a rented RTX 5090 reached PSNR 25.29, and the deployed app serves that scene as a labelled sample. Live: [app](https://wedding-ai-omega.vercel.app)
- **[parameter-golf](https://github.com/jamesEmerson112/parameter-golf/tree/submission/fullstack-headwise-gate)** holds my entries to OpenAI's Parameter Golf challenge for the best language model that fits in 16 MB, where my headwise gated attention submission reports a self-measured three-seed mean of 1.0805 BPB. A later submission appeared to reach 1.0066 BPB until I found its byte accounting inflated and retracted it, and the corrected run scored 1.0972.
- **[watch-and-learn](https://github.com/jamesEmerson112/watch-and-learn)** is a team entry to the MongoDB 2026 hackathon where a user watches and interacts with a Gemini agent driving a browser, and my VoyageAI embedding setup and multi-agent competitor-analysis feature were merged upstream.

### Rust track and open source

- **[Rust-learning](https://github.com/jamesEmerson112/Rust-learning)** is an 80-lesson Rust curriculum I built for myself, where every lesson ships an example binary, a stubbed exercise and an integration test, and two Rust tools render a progress dashboard from the results.
- **[splat-service](https://github.com/jamesEmerson112/splat-service)** is a photos-in, 3D-scene-out service with a Rust and Axum backend that owns the job state machine, a Next.js viewer, and a RunPod GPU worker for COLMAP and Gaussian splat training. The GPU worker is still a Phase 1 stub, so the flow runs end to end today in a zero-credential mock mode.
- **[Ada](https://github.com/machmoon/Ada)** is an open-source AI hardware engineering agent that turns a plain-language board description into a placed and routed KiCad layout, and I contributed eleven merged pull requests, including the Google ADK pipeline rewrite.
- **[jamesemerson112.github.io](https://github.com/jamesEmerson112/jamesemerson112.github.io)** is my portfolio site, a Svelte application that scans my GitHub repositories with scc on a scheduled GitHub Actions run and renders searchable project cards and spider charts from the generated metrics. Live: [site](https://jamesemerson112.github.io)

I also write Rust for private client work, including a deployed Las Vegas nail salon scheduler and an orchard farm booking system still in progress, both built on Axum and SQLx against PostgreSQL.

## Languages and tools

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch" />
  <img src="https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white" alt="CUDA" />
  <img src="https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white" alt="Rust" />
  <img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB" />
  <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=blue" alt="React" />
  <img src="https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white" alt="Express" />
  <img src="https://img.shields.io/badge/Node.JS-339933?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css&logoColor=white" alt="CSS3" />
  <img src="https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E" alt="JavaScript" />
  <img src="https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white" alt="C" />
  <img src="https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white" alt="C++" />
  <img src="https://img.shields.io/badge/C%23-239120?style=for-the-badge" alt="C#" />
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge" alt="Java" />
  <img src="https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white" alt="Go" />
  <img src="https://img.shields.io/badge/Ruby-CC342D?style=for-the-badge&logo=ruby&logoColor=white" alt="Ruby" />
</p>

## GitHub stats

<img src="github-metrics.svg" alt="GitHub metrics generated by lowlighter/metrics" />

## Beyond code

Champion of Basketball 5v5 Intramural Greek Life at University of Nevada, Las Vegas

Experienced player in Squad (50 vs. 50 simulated battlefield). Squad lead at over 50+ matches. Commander at 10+ matches

Ex-President of Shine City volunteer. Vice-President of 25+ club members. Proud member of UNLV Buddies and ACM.

Prompt Engineer since ChatGPT 3.0

Email me at james.emerson.vo.2503@gmail.com if you want to talk about any of this.
