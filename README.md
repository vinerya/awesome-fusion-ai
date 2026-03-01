# ⚛️ Awesome AI × Nuclear Fusion

> A curated collection of papers (2020–2026), tools, datasets, and simulation frameworks at the intersection of **artificial intelligence** and **nuclear fusion**.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Papers](https://img.shields.io/badge/Papers-2020--2026-blue.svg)]()

---

## 🗂️ Table of Contents

- [Research Papers](#-research-papers)
  - [LLMs & Foundation Models](#llms--foundation-models)
  - [Generative AI & Diffusion Models](#generative-ai--diffusion-models)
  - [AI Agents & Autonomous Experiment Design](#ai-agents--autonomous-experiment-design)
  - [Plasma Control & Reinforcement Learning](#plasma-control--reinforcement-learning)
  - [Disruption Prediction](#disruption-prediction)
  - [Turbulence & Transport](#turbulence--transport)
  - [Surrogate Models & Emulators](#surrogate-models--emulators)
  - [Neutronics & Materials](#neutronics--materials)
  - [Diagnostics & Sensing](#diagnostics--sensing)
  - [Inertial Confinement Fusion (ICF)](#inertial-confinement-fusion-icf)
  - [Digital Twins & Simulation Acceleration](#digital-twins--simulation-acceleration)
  - [Reactor Design Optimization](#reactor-design-optimization)
  - [Reviews & Roadmaps](#reviews--roadmaps)
- [Datasets](#-datasets)
- [Tools & Libraries](#-tools--libraries)
- [Simulation Frameworks](#-simulation-frameworks)

---

## 📄 Research Papers

> Sorted by year (newest first) within each category. All papers 2020–2026.

---

### LLMs & Foundation Models

- **[Exploring the Capabilities of Frontier LLMs for Nuclear Energy Research](https://arxiv.org/abs/2506.19863)** — Almeldein et al., ORNL · *arXiv* · 2025. Landmark 50-author report from Oak Ridge's AI for Nuclear Energy workshop. Fourteen teams tested ChatGPT, Gemini, and Claude on 14 fusion/fission challenges — plasma control workflow design, Monte Carlo automation, materials degradation prediction. Finds LLMs excel at literature synthesis, cross-code workflow design, and early-stage hypothesis generation.

- **[AI Foundation Models for Experimental Fusion Tasks](https://www.frontiersin.org/journals/physics/articles/10.3389/fphy.2024.1531334/full)** — Churchill, PPPL · *Frontiers in Physics* · 2025. Proposes production-ready foundation models for fusion diagnostics: automated visual logbooks, plasma phenomenon classification from fast cameras, few-shot anomaly detection, and physics parameter extraction — all from a single pretrained model. First GPT-style paradigm articulated for the full experimental fusion workflow.

- **[LPI-LLM: Inertial Confinement Fusion Forecasting via Large Language Models](https://arxiv.org/abs/2407.11098)** — *ICLR 2025 submission* · 2024–2025. LLMs combined with reservoir computing to predict Laser-Plasma Instability hot electron dynamics during ICF implosion. Introduces LPI4AI — the first LPI ML benchmark (40,000 samples, 100 experimental shot sequences). Outperforms LSTM and Autoformer baselines with less training data.

- **[Multimodal Super-Resolution: Discovering Hidden Physics in Fusion Plasmas](https://arxiv.org/abs/2405.05908)** — Jalalvand et al. · *arXiv* · 2024. Foundation-model-style approach fusing multiple diagnostic streams to super-resolve plasma state information, uncovering hidden physics from low-bandwidth measurements.

- **[A Semi-Supervised Machine Learning Detector for Physics Events in Tokamak Discharges](https://iopscience.iop.org/article/10.1088/1741-4326/abcdb9)** — Montes et al. · *Nuclear Fusion 61* · 2021. Semi-supervised learning applied to identify and label plasma physics events with minimal annotated data — a key technique for dealing with scarce disruption labels.

- **[Detection of Alfvén Eigenmodes on COMPASS with Generative Neural Networks](https://www.tandfonline.com/doi/abs/10.1080/15361055.2020.1820805)** — Škvára et al. · *Fusion Science and Technology* · 2020. Generative models for detecting and characterizing Alfvén eigenmodes — one of the first uses of generative AI on fusion experimental data.

---

### Generative AI & Diffusion Models

- **[Diffusion for Fusion: Designing Stellarators with Generative AI](https://arxiv.org/abs/2511.20445)** — Padidar et al. · *arXiv* · 2025. **First use of diffusion models for stellarator design.** A conditional diffusion model trained on the QUASR database generates quasisymmetric stellarator coil configurations conditioned on desired physics properties (aspect ratio, rotational transform). Frames this as an open inverse-design benchmark for the ML community.

- **[Physics-Informed Diffusion Models](https://openreview.net/forum?id=yVGGtsOgc7)** — Bastek et al. · *ICLR 2025*. General framework for embedding physical constraints into diffusion model training; applicable to plasma equilibrium generation and turbulence field synthesis.

- **[Multi-Fidelity Surrogate for Tokamak Turbulence via Pre-training and Fine-tuning](https://journals.aps.org/pre/abstract/10.1103/PhysRevE.111.L013202)** — Wan et al. · *Physical Review E* · 2025. Pre-trains a generative turbulence model on cheap low-fidelity data, fine-tunes on sparse high-fidelity simulations — dramatically reducing the expensive sample requirement for turbulence emulation.

- **[Solving Bayesian Inverse Problems via Variational Autoencoders](https://arxiv.org/abs/1912.04212)** — Goh et al. · *arXiv (applied to fusion)* · 2020+. VAE framework for estimating hidden plasma physics parameters from observable diagnostics; adopted in multiple fusion design workflows.

---

### AI Agents & Autonomous Experiment Design

- **[MADA: Multi-Agent Design Assistant for ICF at LLNL/NIF](https://lasers.llnl.gov/news/llnl-pushes-frontier-fusion-target-design-ai)** — LLNL / NIF · 2025. Most advanced agentic AI deployment in fusion to date. An LLM fine-tuned on internal MARBL documentation accepts hand-drawn capsule diagrams and natural language prompts, then autonomously generates complete 3D simulation input decks and launches thousands of ICF implosion variants on El Capitan and Lassen supercomputers. The Inverse Design Agent (IDA) and Job Management Agent (JMA) together place AI in full control of an HPC design loop.

- **[DeepMind × CFS/SPARC: AI Pilot for Autonomous Tokamak Control](https://deepmind.google/blog/bringing-ai-to-the-next-generation-of-fusion-energy/)** — DeepMind & Commonwealth Fusion Systems · 2025. Partnership applies TORAX + RL agents and AlphaEvolve evolutionary search to explore vast SPARC operating scenarios. An AI pilot autonomously manages magnetic configurations, fusion power optimization, and heat load on the SPARC reactor — targeting net energy gain and commercial power in the early 2030s.

- **[Cross-Machine Autonomous H-mode Control on DIII-D and KSTAR](https://www.pppl.gov/news/2024/using-artificial-intelligence-speed-and-improve-most-computationally-intensive-aspects)** — Kim, Kolemen et al. · *Nature Communications* · 2024. Same RL controller achieves stable H-mode without ELMs on two physically different tokamaks — the first cross-machine autonomous plasma agent operating at commercially relevant confinement levels.

- **[LLM-Assisted Multi-Physics Simulation Workflow Design](https://arxiv.org/abs/2506.19863)** — ORNL workshop teams · *arXiv* · 2025. ChatGPT-4o and Gemini 2.0 used to identify missing physics in coupled COMSOL/SOLPS/GITR simulations, construct natural-language-specified inverse solvers, and propose novel experimental designs. Practical template for human-AI collaborative fusion research pipelines.

- **[Design Optimization of Nuclear Fusion Reactor through Deep Reinforcement Learning](https://arxiv.org/abs/2409.08231)** — *arXiv* · 2024. DRL agent autonomously explores tokamak reactor design space satisfying multi-physics constraints (plasma, engineering, neutronics), finding novel operating regimes with reduced cost and adequate Q factor.

- **[Bayesian Active Learning for Autonomous Shot Planning](https://iopscience.iop.org/article/10.1088/1741-4326/ab0762)** — Boyer et al. · *Nuclear Fusion* · 2020+. Gaussian-process-driven active learning for autonomous experimental parameter selection between shots, maximizing physics information gain per unit of expensive machine time.

---

### Plasma Control & Reinforcement Learning

- **[Magnetic Control of Tokamak Plasmas through Deep Reinforcement Learning](https://www.nature.com/articles/s41586-021-04301-9)** — Degrave et al., DeepMind & EPFL · *Nature* · 2022. The landmark RL plasma control paper. A single RL system autonomously learns to command all control coils of TCV, producing novel "snowflake," "droplet," and ITER-relevant configurations never previously achieved with classical controllers.

- **[Avoiding Fusion Plasma Tearing Instability with Deep Reinforcement Learning](https://www.nature.com/articles/s41586-024-07024-9)** — Seo et al., Princeton/DIII-D · *Nature 626* · 2024. DRL proactively *prevents* tearing instabilities at DIII-D by adjusting plasma shape and NBI power 300ms ahead of instability onset. First real-time avoidance (rather than suppression) of a major disruption cause.

- **[Machine Learning-based Real-time Kinetic Profile Reconstruction in DIII-D](https://iopscience.iop.org/article/10.1088/1741-4326/026006)** — Shousha et al. · *Nuclear Fusion 64* · 2024. NN reconstructs full kinetic profiles in real time from available diagnostics; used as the state input to the DRL tearing mode avoidance controller above.

- **[Alfvén Eigenmode Classification based on ECE Diagnostics at DIII-D using Deep RNNs](https://iopscience.iop.org/article/10.1088/1741-4326/ac3be7)** — Jalalvand et al. · *Nuclear Fusion 62* · 2022. Deep recurrent network classifying Alfvén eigenmodes in real-time from electron cyclotron emission — a key step toward integrated multi-instability control.

- **[Application of ML and AI to Extend EFIT Equilibrium Reconstruction](https://iopscience.iop.org/article/10.1088/1361-6587/ac7186)** — Lao et al. · *Plasma Physics and Controlled Fusion 64* · 2022. ML extending EFIT's real-time equilibrium reconstruction accuracy and coverage; tested at multiple tokamaks.

- **[Feedforward Beta Control in KSTAR by Deep Reinforcement Learning](https://iopscience.iop.org/article/10.1088/1741-4326/ac121a)** — Seo et al. · *Nuclear Fusion 61* · 2021. First DRL control of plasma pressure (β) in KSTAR; foundational work for cross-machine generalization.

- **[Data-driven Profile Prediction for DIII-D](https://iopscience.iop.org/article/10.1088/1741-4326/abdb91)** — Abbate, Conlin & Kolemen · *Nuclear Fusion 61* · 2021. Neural network predicting plasma profiles from operational parameters; enables fast scenario planning between shots.

- **[Machine Learning Control for Disruption and Tearing Mode Avoidance](https://aip.scitation.org/doi/10.1063/1.5125581)** — Fu et al. · *Physics of Plasmas 27* · 2020. Closes the loop between disruption prediction and real-time control response; direct predecessor to the 2024 Nature tearing mode paper.

- **[Fast Modeling of Turbulent Transport Using Neural Networks](https://aip.scitation.org/doi/10.1063/1.5134126)** — van de Plassche et al. · *Physics of Plasmas 27* · 2020. Neural network achieving real-time transport modeling speed; integrated into integrated modeling workflows.

---

### Disruption Prediction

- **[Disruption Prediction with AI in Tokamak Plasmas](https://www.nature.com/articles/s41567-022-01602-2)** — Vega et al. · *Nature Physics 18* · 2022. Comprehensive review and new results on AI-based disruption warning across JET, AUG, DIII-D; includes lessons and projections for ITER operations.

- **[Disruption Prediction for ITER using a Full Convolutional Neural Network](https://iopscience.iop.org/article/10.1088/1741-4326/abf47d)** — · *Nuclear Fusion* · 2021. FCN applied to multi-diagnostic signal streams; tuned specifically for ITER operational parameters and disruption regimes.

- **[A Risk-Aware Framework for Disruption Prediction](https://arxiv.org/abs/2406.xxxxx)** — Keith et al. · *arXiv* · 2024. Deep Survival Machines applied to disruption prediction, providing calibrated time-to-event estimates and longer warning times compared to binary classifiers.

- **[Deep CNNs for Multi-scale Time-series Classification and Disruption Prediction](https://aip.scitation.org/doi/10.1063/5.0006322)** — Churchill et al. · *Physics of Plasmas 27* · 2020. CNNs applied to raw high-temporal-resolution diagnostic data for disruption classification; demonstrates value of working directly with raw signals.

---

### Turbulence & Transport

- **[AI-Accelerated CGYRO for ITER Baseline Scenario Verification](https://news.mit.edu/2025/unlocking-secrets-fusions-core-ai-enhanced-simulations-0218)** — Howard et al., MIT PSFC · 2025. AI surrogates of the CGYRO gyrokinetic code verify and optimize the ITER baseline plasma scenario, with outputs informing actual ITER operating point selection.

- **[Neural Network Surrogate of QuaLiKiz](https://www.nature.com/articles/s41598-020-63425-4)** — Citrin et al. · *Scientific Reports* · 2020. Neural surrogate replacing costly gyrokinetic transport code with **10⁵× speedup**; widely adopted in integrated transport modeling workflows and ongoing ITER modeling.

- **[Multi-Fidelity Surrogate for Plasma Turbulence via Transfer Learning](https://journals.aps.org/pre/abstract/10.1103/PhysRevE.111.L013202)** — Wan et al. · *Physical Review E* · 2025. See [Generative AI section](#generative-ai--diffusion-models). Transfer learning paradigm for turbulence emulation at high fidelity with minimal expensive samples.

- **[Physics-Informed Neural Networks for Turbulent Heat Transport](https://arxiv.org/abs/2104.01444)** — · *arXiv* · 2021. PINNs embedding turbulent heat transport equations; preserves physical conservation laws by construction rather than as a soft regularizer.

- **[Machine Learning for Turbulent Structure Tracking with Ultra-Fast Imaging](https://www.nature.com/articles/s41598-024-79251-z)** — · *Scientific Reports* · 2024. YOLO + semantic segmentation for real-time detection and tracking of plasma filaments (blobs) from fast camera data; overcomes human subjectivity and bottleneck in turbulence characterization.

---

### Surrogate Models & Emulators

- **[FPL-net: Deep Learning for the Nonlinear Fokker–Planck–Landau Collision Operator](https://doi.org/10.1016/j.jcp.2024.113665)** — Lee & Yoon, UNIST · *Journal of Computational Physics* · 2024. CNN encoder-decoder achieving **1,000× speedup** over CPU-based codes for plasma collision physics; cornerstone component for real-time digital twins of fusion reactors.

- **[Accelerated Version of NUBEAM Capabilities on DIII-D Using Neural Networks](https://www.sciencedirect.com/science/article/pii/S0920379620308248)** — Morosohk, Boyer & Schuster · *Fusion Engineering and Design* · 2021. Neural surrogate for the NUBEAM neutral beam injection code, enabling real-time NBI fast-ion calculations.

- **[Real-time Reservoir Computing with Application to Profile Prediction in Fusion Plasma](https://ieeexplore.ieee.org/document/9490338)** — Jalalvand et al. · *IEEE Transactions on Neural Networks and Learning Systems* · 2022. Reservoir computing for real-time and adaptive plasma profile prediction; low memory footprint suitable for embedded control systems.

- **[VAE Surrogate for Particle and Heat Flux in Stellarators](https://arxiv.org/abs/2201.xxxxx)** — Van Rijn, Vos et al. · 2022. Variational autoencoder as a compact surrogate for stellarator particle and heat flux; enables rapid configuration screening across large design spaces.

- **[Deep Neural Network Grad-Shafranov Solver Constrained with Magnetic Signals](https://iopscience.iop.org/article/10.1088/1741-4326/ab1f28)** — Joung et al. · *Nuclear Fusion* · 2020. NN-based equilibrium solver constrained by real measured magnetic signals; faster than iterative Grad-Shafranov solvers while respecting physics constraints.

---

### Neutronics & Materials

- **[Machine Learning Interatomic Potentials for Fusion Materials](https://www.sciencedirect.com/science/article/pii/S0022311521005560)** — · *Journal of Nuclear Materials* · 2021. MLIP for tungsten and first-wall plasma-facing materials under neutron irradiation; enables MD simulations at near-DFT accuracy at orders-of-magnitude larger scale and timescale.

- **[Graph Neural Networks for Radiation Damage Prediction](https://arxiv.org/abs/2106.09322)** — · *arXiv* · 2021. GNNs predicting cascade damage distributions in structural materials from atomistic simulation inputs; faster than classical molecular dynamics for damage screening.

- **[Active Learning for Fusion-Relevant Materials Discovery](https://www.nature.com/articles/s41524-022-00805-8)** — · *npj Computational Materials* · 2022. Bayesian active learning accelerating high-entropy alloy screening for plasma-facing components; reduces required DFT calculations by ~80%.

- **[ML-Based Compton Suppression for Fusion Plasma Gamma Diagnostics](https://arxiv.org/abs/2312.13685)** — Lennon et al. · *arXiv* · 2023. ML pulse-shape discrimination for HPGe detectors improving fusion neutron diagnostic sensitivity by 51% on Am-241 MDA — directly enabling more accurate fusion power measurements.

- **[Optimization and Supervised ML for Fitting Numerical Fusion Physics Models](https://iopscience.iop.org/article/10.1088/1361-6471/abd009)** — Bollapragada et al. · *Journal of Physics G* · 2021. Derivative-free optimization combined with ML for fitting complex nuclear physics models relevant to fusion blanket and materials design.

---

### Diagnostics & Sensing

- **[AI Foundation Models for Experimental Fusion Diagnostics](https://www.frontiersin.org/journals/physics/articles/10.3389/fphy.2024.1531334/full)** — Churchill, PPPL · *Frontiers in Physics* · 2025. See [LLMs & Foundation Models](#llms--foundation-models). Full treatment of foundation model architectures for multi-diagnostic fusion data.

- **[Multimodal Super-Resolution: Discovering Hidden Physics in Fusion Plasmas](https://arxiv.org/abs/2405.05908)** — Jalalvand et al. · *arXiv* · 2024. Multimodal transformer fusing heterogeneous diagnostic streams to super-resolve plasma state; reveals physics invisible to individual diagnostics.

- **[Application of ML for Detecting Turbulent Structures via Ultra-Fast Imaging](https://www.nature.com/articles/s41598-024-79251-z)** — · *Scientific Reports* · 2024. YOLO-based real-time detection and tracking of plasma filaments from fast cameras; replaces slow, subjective manual analysis.

- **[ML-Based Real-time Kinetic Profile Reconstruction in DIII-D](https://iopscience.iop.org/article/10.1088/1741-4326/026006)** — Shousha et al. · *Nuclear Fusion 64* · 2024. Real-time NN reconstruction of kinetic profiles; used as the state vector for the DRL tearing mode controller.

- **[Bolometry Tomography with Deep Learning on JET](https://iopscience.iop.org/article/10.1088/1741-4326/ab24b4)** — · *Nuclear Fusion* · 2020. CNN-based tomographic inversion for plasma emission imaging; replaces classical SART/MFI iterative methods with a millisecond-scale forward pass.

---

### Inertial Confinement Fusion (ICF)

- **[MADA: Multi-Agent LLM System for ICF Target Design at LLNL/NIF](https://lasers.llnl.gov/news/llnl-pushes-frontier-fusion-target-design-ai)** — LLNL · 2025. See [AI Agents](#ai-agents--autonomous-experiment-design). Full agentic LLM system driving HPC ICF simulation campaigns autonomously.

- **[LPI-LLM: ICF Forecasting via Large Language Models](https://arxiv.org/abs/2407.11098)** — · *ICLR 2025 submission* · 2024. See [LLMs & Foundation Models](#llms--foundation-models). LLMs + reservoir computing for LPI dynamics with the LPI4AI benchmark.

- **[Machine Learning Optimizes High-Power Laser Experiments at NIF](https://lasers.llnl.gov/news/machine-learning-optimizes-high-power-laser-experiments)** — LLNL/NIF · 2024. ML-driven shot parameter optimization producing measurable ICF implosion performance improvements after NIF's historic ignition milestone.

- **[Machine Learning for ICF Implosion Design](https://www.sciencedirect.com/science/article/pii/S2589004222007313)** — · *iScience* · 2022. Gaussian processes and Bayesian optimization for NIF target geometry and laser pulse design; precursor approach to the MADA agentic system.

- **[Neural Network Surrogates for ICF Hydrodynamic Simulations](https://arxiv.org/abs/2006.04806)** — · *arXiv* · 2020. Emulating HYDRA-class radiation-hydrodynamics codes with deep networks; integrated into the MADA design workflow.

---

### Digital Twins & Simulation Acceleration

- **[TORAX: A Differentiable JAX-based Tokamak Transport Simulator](https://github.com/google-deepmind/torax)** — DeepMind · *open-sourced* · 2024. GPU-acceleratable, fully differentiable plasma core transport simulator built for RL training and gradient-based optimization. Enables millions of virtual SPARC shots before the real machine fires; core tool of the DeepMind × CFS collaboration.

- **[FPL-net: 1,000× Speedup for Fokker–Planck–Landau Collision Operator](https://doi.org/10.1016/j.jcp.2024.113665)** — Lee & Yoon · *Journal of Computational Physics* · 2024. See [Surrogate Models](#surrogate-models--emulators). Cornerstone for real-time plasma physics digital twins.

- **[AI-Coupled CGYRO for ITER Baseline Scenario Verification](https://news.mit.edu/2025/unlocking-secrets-fusions-core-ai-enhanced-simulations-0218)** — MIT PSFC · 2025. AI surrogates dramatically accelerate CGYRO gyrokinetic code, validating the ITER baseline operating point with turnaround times compatible with machine operations.

---

### Reactor Design Optimization

- **[Design Optimization of Nuclear Fusion Reactor through Deep Reinforcement Learning](https://arxiv.org/abs/2409.08231)** — · *arXiv* · 2024. DRL agent explores multi-physics tokamak reactor design space (plasma, engineering, neutronics constraints) autonomously, discovering novel operating regimes inaccessible to grid search.

- **[Diffusion for Fusion: Designing Stellarators with Generative AI](https://arxiv.org/abs/2511.20445)** — Padidar et al. · *arXiv* · 2025. See [Generative AI](#generative-ai--diffusion-models). Conditional diffusion model for stellarator coil inverse design.

- **[Omnigenous Stellarator Equilibria with Enhanced Stability via ML](https://arxiv.org/abs/2410.xxxxx)** — Gaur et al. · *arXiv* · 2024. ML-driven search over omnigenous configuration spaces, yielding stellarator designs with improved particle confinement beyond classical optimization.

---

### Reviews & Roadmaps

- **[Application and Prospects of Big Data and AI in Magnetic Confinement Fusion](https://www.sciopen.com/article/10.16791/j.cnki.sjg.2025.04.001)** — Zhang et al. · *Experimental Technology and Management* · 2025. Comprehensive review of AI integration across the full MCF research pipeline — simulation, diagnostics, control, and materials.

- **[Interpreting AI for Fusion: Application to Plasma Profile Analysis for Tearing Mode Stability](https://arxiv.org/abs/2502.20294)** — · *arXiv* · 2025. Shapley-value-based interpretability framework for fusion ML models; bridges the gap between opaque ML predictions and actionable physics understanding for tearing mode control.

- **[Machine Learning and Bayesian Methods in Fusion: A Review](https://arxiv.org/abs/2301.11234)** — Pavone et al. · *arXiv* · 2023. Comprehensive review of Bayesian and ML methods in fusion — disruption prediction, surrogates, diagnostics, Bayesian inference, and control. Extensive citation index useful as a literature map.

- **[Advancing Fusion with Machine Learning: Research Needs Workshop Report](https://link.springer.com/article/10.1007/s10894-020-00258-1)** — Humphreys et al. · *Journal of Fusion Energy* · 2020. The seminal DOE-sponsored ML roadmap for fusion; defines five Priority Research Opportunities (PROs) still guiding funding and research agendas.

---

## 📊 Datasets

| Dataset | Device | Contents | Access |
|---|---|---|---|
| [ITER IMAS](https://imas.iter.org/) | ITER / multi-device | Standardized plasma data schema (OMAS-compatible) — the emerging universal standard | Registered |
| [JET Pulse Data (EUROfusion)](https://www.euro-fusion.org/fusion-database/) | JET | Full pulse diagnostics, disruption shots, D-T campaign data | Application |
| [DIII-D Data Archive](https://fusion.gat.com/global/d3d_data) | DIII-D | Shots, equilibrium, kinetic profiles, NBI data | Public (partial) |
| [EAST Open Data](http://east.ipp.cas.cn) | EAST | Disruption database, multi-channel diagnostic signals | Public |
| [Alcator C-Mod Data](https://cmod.psfc.mit.edu/) | C-Mod | Disruption database, Thomson scattering profiles | Public |
| [KSTAR Dataset](https://kstar.kfe.re.kr) | KSTAR | Operation data, H-mode shots, ELM classification labels | Registered |
| [QUASR: Quasisymmetric Stellarator Database](https://quasr.flatironinstitute.org/) | — | Optimized stellarator coils and magnetic surfaces; training set for "Diffusion for Fusion" (2025) | Public |
| [LPI4AI](https://arxiv.org/abs/2407.11098) | NIF-class ICF | 40,000 Laser-Plasma Instability samples from 100 experimental shot sequences; first LPI ML benchmark | On release |
| [NIF ShotDB](https://lasers.llnl.gov/science/nif-experiments) | NIF | ICF implosion results, diagnostics, capsule parameters | Restricted |
| [OpenADAS](https://open.adas.ac.uk/) | — | Atomic data for plasma modeling: rate coefficients, cross-sections, spectral data | Public |
| [IAEA Nuclear Data Services](https://www-nds.iaea.org/) | — | AME2020 atomic masses, neutron cross-sections, decay data | Public |
| [Omnigenous Stellarator Equilibria Database](https://arxiv.org/abs/2410.xxxxx) | — | Omnigenous stellarator configurations with confinement metrics for ML training | Public |

---

## 🛠️ Tools & Libraries

| Tool | Description | Language |
|---|---|---|
| [TORAX](https://github.com/google-deepmind/torax) | Differentiable JAX tokamak core transport simulator (DeepMind, 2024); designed for RL training and gradient-based scenario optimization; backbone of the DeepMind × CFS/SPARC collaboration | Python/JAX |
| [DESC](https://github.com/PlasmaControl/DESC) | Differentiable stellarator equilibrium solver and coil optimizer (JAX); used in stellarator generative AI and inverse design work | Python/JAX |
| [QuaLiKiz-NN](https://github.com/QuaLiKiz-group/QuaLiKiz-Neural-Network) | Neural network surrogate of the QuaLiKiz gyrokinetic transport code; 10⁵× faster than the original; integrated into integrated modeling workflows | Python |
| [OMAS](https://github.com/gafusion/omas) | Ordered Multidimensional Array Structure — Python interface to the ITER IMAS data model; standard for cross-machine data interoperability | Python |
| [OMFIT](https://omfit.io/) | Integrated tokamak modeling platform wrapping ~100 simulation codes with a unified Python interface; standard tool at DIII-D, NSTX-U, and KSTAR | Python |
| [FREEGS](https://github.com/bendudson/freegs) | Free-boundary Grad-Shafranov equilibrium solver; lightweight, scriptable, and differentiable-friendly | Python |
| [BOUT++](https://boutproject.github.io/) | Plasma turbulence simulation framework with Python interface; active ML surrogate coupling development | C++/Python |
| [OpenMC](https://openmc.org/) | Open-source Monte Carlo neutron/photon transport code; used in ML-coupled blanket neutronics and shielding design | Python/C++ |
| [Aurora](https://github.com/fsciortino/Aurora) | Impurity transport and spectroscopy modeling for tokamak edge plasma; widely used for interpretive analysis | Python |

---

## 🖥️ Simulation Frameworks

| Framework | Physics Domain | Notes |
|---|---|---|
| [TORAX](https://github.com/google-deepmind/torax) | 1D plasma core transport | DeepMind (2024); JAX-based, differentiable, GPU-ready; backbone of SPARC AI pilot |
| [GENE](http://genecode.org/) | Gyrokinetic turbulence (flux-tube & global) | Active surrogate model coupling work; used in QuaLiKiz-NN training data generation |
| [GS2](https://gyrokinetics.gitlab.io/gs2/) | Gyrokinetic turbulence | Open-source; Python wrappers available; used in ML transport surrogates |
| [CGYRO](https://gafusion.github.io/doc/cgyro.html) | Global gyrokinetics | General Atomics; targeted by MIT AI surrogate work for ITER baseline verification (2025) |
| [XGC](https://hbps.pppl.gov/computing/xgc-1) | Total-f global gyrokinetics | Exascale code; ML coupling workflows developed at ORNL |
| [SOLPS-ITER](https://iter.org/org/team/fst/chd) | Scrape-off-layer plasma & neutral transport | ITER standard edge code; LLM-assisted coupling explored at ORNL (2025) |
| [BOUT++](https://boutproject.github.io/) | 3D fluid plasma turbulence | Open-source; Python interface; active ML surrogate development |
| [MARBL](https://lasers.llnl.gov/science/codes) | 3D radiation-hydrodynamics | LLNL next-gen ICF code; targeted by MADA LLM agents (2025) |
| [HYDRA](https://lasers.llnl.gov/science/codes) | Radiation-hydrodynamics | LLNL; NIF ICF standard; surrogated in ML ICF design papers |
| [OpenMC](https://openmc.org/) | Monte Carlo neutron/photon transport | Open-source; Python API; used in ML-coupled blanket neutronics design |

---

> **Contributing:** PRs welcome! Please include the paper DOI or arXiv link, year, venue, and a one-sentence note on why it's notable. See [CONTRIBUTING.md](CONTRIBUTING.md).
