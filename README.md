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

- **[TokaMind: A Multi-Modal Transformer Foundation Model for Tokamak Plasma Dynamics](https://arxiv.org/abs/2602.15084)** — Boschi, Loreti, Amorisco et al., UK Atomic Energy Authority / IBM Research · *arXiv* · 2026. The first open-source multi-modal transformer foundation model for tokamak plasma data (time-series, 2D profiles, video), pretrained on MAST data with robust missing-signal handling; fine-tuning beats task-specific baselines on nearly all tasks in the companion **[TokaMark](https://arxiv.org/abs/2602.10132)** benchmark (Rousseau et al., UKAEA/IBM, 2026) — a standardized, openly-released 14-task evaluation suite for fusion foundation models.

- **[FusionMAE: Large-Scale Pretrained Model to Optimize and Simplify Diagnostic and Control of Fusion Plasma](https://arxiv.org/abs/2509.12945)** — Yang, Yang, Tian et al., Southwestern Institute of Physics (HL-3 tokamak) · *arXiv*, also published as *Communications Physics* · 2025–2026. A masked-autoencoder foundation model pretrained on 2,445 HL-3 discharges, compressing 88 diagnostic signals into one embedding; reconstructs missing diagnostics with ~97% accuracy, acting as a "virtual backup diagnostic," and transfers to disruption prediction and equilibrium reconstruction.

- **[Exploring the Capabilities of Frontier LLMs for Nuclear Energy Research](https://arxiv.org/abs/2506.19863)** — Almeldein et al., ORNL · *arXiv* · 2025. Landmark 50-author report from Oak Ridge's AI for Nuclear Energy workshop. Fourteen teams tested ChatGPT, Gemini, and Claude on 14 fusion/fission challenges — plasma control workflow design, Monte Carlo automation, materials degradation prediction. Finds LLMs excel at literature synthesis, cross-code workflow design, and early-stage hypothesis generation.

- **[AI Foundation Models for Experimental Fusion Tasks](https://www.frontiersin.org/journals/physics/articles/10.3389/fphy.2024.1531334/full)** — Churchill, PPPL · *Frontiers in Physics* · 2025. Proposes production-ready foundation models for fusion diagnostics: automated visual logbooks, plasma phenomenon classification from fast cameras, few-shot anomaly detection, and physics parameter extraction — all from a single pretrained model. TokaMind and FusionMAE (above) are the first concrete large-scale implementations of this vision.

- **[LPI-LLM: Inertial Confinement Fusion Forecasting via Large Language Models](https://arxiv.org/abs/2407.11098)** — *ICLR 2025 submission* · 2024–2025. LLMs combined with reservoir computing to predict Laser-Plasma Instability hot electron dynamics during ICF implosion. Introduces LPI4AI — the first LPI ML benchmark (40,000 samples, 100 experimental shot sequences). Outperforms LSTM and Autoformer baselines with less training data.

- **[Multimodal super-resolution: discovering hidden physics and its application to fusion plasmas](https://www.nature.com/articles/s41467-025-63492-1)** — Jalalvand, Kim, Seo, Hu, Curie, Steiner, Nelson, Na & Kolemen, Princeton University / PPPL / Chung-Ang University / Columbia / Seoul National University · *Nature Communications* · 2025. The "Diag2Diag" model fuses multiple DIII-D diagnostics to generate super-resolution Thomson-scattering-equivalent data from faster sensors, revealing magnetic-island ELM-suppression dynamics invisible to any single instrument.

- **[A Semi-Supervised Machine Learning Detector for Physics Events in Tokamak Discharges](https://iopscience.iop.org/article/10.1088/1741-4326/abcdb9)** — Montes et al. · *Nuclear Fusion 61* · 2021. Semi-supervised learning applied to identify and label plasma physics events with minimal annotated data — a key technique for dealing with scarce disruption labels.

- **[Detection of Alfvén Eigenmodes on COMPASS with Generative Neural Networks](https://www.tandfonline.com/doi/abs/10.1080/15361055.2020.1820805)** — Škvára et al. · *Fusion Science and Technology* · 2020. Generative models for detecting and characterizing Alfvén eigenmodes — one of the first uses of generative AI on fusion experimental data.

---

### Generative AI & Diffusion Models

- **[Data-Driven Generation of Compact Quasi-Isodynamic Stellarators](https://arxiv.org/abs/2608.16938)** — Han et al., Institute of Plasma Physics, Chinese Academy of Sciences / USTC · *arXiv* · 2026. Extends the ConStellaration conditional boundary-generation approach to four-field-period QI stellarators in the sparsely-sampled low-aspect-ratio regime, cutting compact-domain test loss ~87% and yielding converged ultra-compact candidates. See [Reactor Design Optimization](#reactor-design-optimization) for the underlying ConStellaration dataset.

- **[Optimal-Transport-Guided Functional Flow Matching for Turbulent Field Generation in Hilbert Space](https://arxiv.org/abs/2604.05700)** — Li, Wan, Qu et al. · *arXiv* · 2026. Generative flow-matching model treating turbulent fields as elements of an infinite-dimensional Hilbert space; benchmarked on both Navier–Stokes flow and the Hasegawa–Wakatani plasma turbulence system, producing deterministic noise-to-data generation paths for turbulence field synthesis.

- **[Diffusion for Fusion: Designing Stellarators with Generative AI](https://arxiv.org/abs/2511.20445)** — Padidar et al. · *arXiv* · 2025. **First use of diffusion models for stellarator design.** A conditional diffusion model trained on the QUASR database generates quasisymmetric stellarator coil configurations conditioned on desired physics properties (aspect ratio, rotational transform). Frames this as an open inverse-design benchmark for the ML community.

- **[Reconstructing High-Fidelity Plasma Turbulence with Data-Driven Tuning of Diffusion in Low-Resolution Grids](https://arxiv.org/abs/2509.11576)** — Li et al. · *arXiv* · 2025. Physics-informed neural networks learn diffusion/hyper-diffusion closure coefficients for the Hasegawa–Wakatani plasma turbulence model, reproducing high-resolution DNS spectral/flux statistics at one-eighth the spatial resolution (10× speedup) and uncovering inverse-transport regimes absent from conventional closures.

- **[Physics-Informed Diffusion Models](https://openreview.net/forum?id=yVGGtsOgc7)** — Bastek et al. · *ICLR 2025*. General framework for embedding physical constraints into diffusion model training; applicable to plasma equilibrium generation and turbulence field synthesis.

- **[Multi-Fidelity Surrogate for Tokamak Turbulence via Pre-training and Fine-tuning](https://journals.aps.org/pre/abstract/10.1103/PhysRevE.111.L013202)** — Wan et al. · *Physical Review E* · 2025. Pre-trains a generative turbulence model on cheap low-fidelity data, fine-tunes on sparse high-fidelity simulations — dramatically reducing the expensive sample requirement for turbulence emulation.

- **[Solving Bayesian Inverse Problems via Variational Autoencoders](https://arxiv.org/abs/1912.04212)** — Goh et al. · *arXiv (applied to fusion)* · 2020+. VAE framework for estimating hidden plasma physics parameters from observable diagnostics; adopted in multiple fusion design workflows.

---

### AI Agents & Autonomous Experiment Design

- **[PPPL to Lead Genesis Mission Project to Create an AI Operator for a Crucial Fusion Energy Heating System](https://www.pppl.gov/news/2026/pppl-lead-genesis-mission-project-create-ai-operator-crucial-fusion-energy-heating-system)** — Princeton Plasma Physics Laboratory (PI: Syun'ichi Shiraiwa), with Rice University, Naval Research Lab, Brookhaven, Sophelio · DOE Genesis Mission · July 2026. Develops an AI system to **autonomously operate** high-power gyrotrons for electron cyclotron heating, paired with a digital twin of gyrotron physics — a directly funded instance of autonomous tokamak subsystem operation.

- **[PPPL Launches STELLAR-AI Platform to Accelerate Fusion Energy Research](https://www.pppl.gov/news/2026/pppl-launches-stellar-ai-platform-accelerate-fusion-energy-research)** — Princeton Plasma Physics Laboratory, with MIT, U. Wisconsin–Madison, NVIDIA, Microsoft, Commonwealth Fusion Systems, General Atomics, Type One Energy, Realta Fusion & UKAEA · DOE Genesis Mission · January 2026. New CPU/GPU/QPU computing platform connecting AI/HPC directly to live experimental devices (NSTX-U) for real-time analysis and AI-driven stellarator configuration optimization; expanded internationally in September 2026 via the SUNRISE–STELLAR-AI Federation with UKAEA's MAST Upgrade.

- **[Multi-Agent Design Assistant for the Simulation of Inertial Fusion Energy](https://arxiv.org/abs/2510.17830)** — Shachar, Sterbentz, Menon, Jekel, Fernández-Godino, Brown, Boureima, Hao, Korner, Rieben, White, Schill & Belof, LLNL / Sandia National Laboratories / Los Alamos National Laboratory · *arXiv* (announced by [LLNL](https://lasers.llnl.gov/news/llnl-pushes-frontier-fusion-target-design-ai), Aug. 2025) · 2025. Most advanced agentic AI deployment in fusion to date. "MADA" pairs an LLM-driven Inverse Design Agent (IDA) with a Job Management Agent (JMA): an LLM fine-tuned on internal MARBL documentation accepts a hand-drawn capsule diagram and a natural-language prompt, then autonomously generates complete 3D simulation input decks and launches thousands of ICF implosion variants on the El Capitan and Tuolumne supercomputers — achieving simulated ignition via fully autonomous inverse design. See [ICF](#inertial-confinement-fusion-icf).

- **[DeepMind × CFS/SPARC: AI Pilot for Autonomous Tokamak Control](https://deepmind.google/blog/bringing-ai-to-the-next-generation-of-fusion-energy/)** — DeepMind & Commonwealth Fusion Systems · 2025. Partnership applies TORAX + RL agents and AlphaEvolve evolutionary search to explore vast SPARC operating scenarios. An AI pilot autonomously manages magnetic configurations, fusion power optimization, and heat load on the SPARC reactor — targeting net energy gain and commercial power in the early 2030s.

- **[Cross-Machine Autonomous H-mode Control on DIII-D and KSTAR](https://www.pppl.gov/news/2024/using-artificial-intelligence-speed-and-improve-most-computationally-intensive-aspects)** — Kim, Kolemen et al. · *Nature Communications* · 2024. Same RL controller achieves stable H-mode without ELMs on two physically different tokamaks — the first cross-machine autonomous plasma agent operating at commercially relevant confinement levels.

- **[LLM-Assisted Multi-Physics Simulation Workflow Design](https://arxiv.org/abs/2506.19863)** — ORNL workshop teams · *arXiv* · 2025. ChatGPT-4o and Gemini 2.0 used to identify missing physics in coupled COMSOL/SOLPS/GITR simulations, construct natural-language-specified inverse solvers, and propose novel experimental designs. Practical template for human-AI collaborative fusion research pipelines.

- **[Design Optimization of Nuclear Fusion Reactor through Deep Reinforcement Learning](https://arxiv.org/abs/2409.08231)** — *arXiv* · 2024. DRL agent autonomously explores tokamak reactor design space satisfying multi-physics constraints (plasma, engineering, neutronics), finding novel operating regimes with reduced cost and adequate Q factor.

- **[Bayesian Active Learning for Autonomous Shot Planning](https://iopscience.iop.org/article/10.1088/1741-4326/ab0762)** — Boyer et al. · *Nuclear Fusion* · 2020+. Gaussian-process-driven active learning for autonomous experimental parameter selection between shots, maximizing physics information gain per unit of expensive machine time.

---

### Plasma Control & Reinforcement Learning

- **[Enabling Integrated AI Control on DIII-D: A Control System Design with State-of-the-Art Experiments](https://iopscience.iop.org/article/10.1088/1741-4326/ae7f9d)** — Rothstein et al., Princeton University & PPPL · *Nuclear Fusion 66*, 076050 · 2026. Introduces PACMAN, a real-time ML control framework deployed across five DIII-D experiment types (RL control of non-inductive plasmas, tearing-mode suppression, ELM prediction, Alfvén eigenmode control, MPC profile management) — an integrated platform rather than a single-purpose controller.

- **[Demonstration of Reconstruction-Free Static Magnetic Control of DIII-D Plasma with Deep Reinforcement Learning](https://iopscience.iop.org/article/10.1088/1741-4326/ae34c6)** — Subbotin et al., Next Step Fusion / UC San Diego / General Atomics · *Nuclear Fusion 66*, 026040 · 2026. A Soft Actor-Critic RL controller maps raw magnetic diagnostics directly to actuator commands, bypassing equilibrium reconstruction entirely, achieving 1.5–2.0 cm shape control precision in real DIII-D experiments.

- **[Isoflux Plasma Shape Control Under Large Transient Disturbances on EAST via Reinforcement Learning](https://iopscience.iop.org/article/10.1088/1741-4326/ae8313)** — Zhang et al., Institute of Plasma Physics CAS / USTC · *Nuclear Fusion 66*, 086012 · 2026. A DRL controller trained in a disturbance-rich simulation improves EAST's isoflux shape-control robustness under large transient errors where fixed-gain PID saturates.

- **[Real-Time Virtual Circuits for Plasma Shape Control via Neural Network Emulators: Experimental Demonstration on MAST Upgrade](https://arxiv.org/abs/2608.28468)** — Amorisco, Pentland, Agnello et al., UKAEA Culham · *arXiv* · 2026. First experimental deployment of NN-emulated "virtual circuits" computed live (replacing offline lookup tables) for interpretable shape control on MAST-U, trained on a library of over one million simulated equilibria.

- **[Learning Plasma Dynamics and Robust Rampdown Trajectories with Predict-First Experiments at TCV](https://www.nature.com/articles/s41467-025-63917-x)** — Wang, Pau, Rea, Felici et al., MIT PSFC, EPFL & Commonwealth Fusion Systems · *Nature Communications* · 2025. Direct follow-on to the DeepMind/EPFL TCV lineage: a neural state-space model plus RL designs shutdown trajectories, validated live on TCV with a "predict-first" shot that safely exceeded prior operational current limits by 20%.

- **[Plasma Shape Control via Zero-Shot Generative Reinforcement Learning](https://arxiv.org/abs/2510.17531)** — Wu et al., Zhejiang University & Southwestern Institute of Physics · *arXiv* · 2025. Combines GAIL with Hilbert-space representation learning on historical PID-discharge data to produce a foundation policy deployable zero-shot across diverse shape-tracking tasks without per-task fine-tuning.

- **[Active Ramp-Down Control and Trajectory Design for Tokamaks with Neural Differential Equations and Reinforcement Learning](https://www.nature.com/articles/s42005-025-02146-6)** — Wang, Rea, So, Fan et al., MIT PSFC · *Communications Physics* · 2025. A hybrid physics/neural-ODE simulator of SPARC-like ramp-downs, massively parallelized on GPU with randomized physics, trains an RL policy that both controls in real time and generates offline trajectory libraries avoiding disruption-correlated limits.

- **[High-Fidelity Data-Driven Dynamics Model for Reinforcement Learning-Based Control in HL-3 Tokamak](https://www.nature.com/articles/s42005-025-02302-y)** — Wu et al., Southwestern Institute of Physics & Zhejiang University · *Communications Physics* · 2025. A fully data-driven, compounding-error-corrected simulator plus an EFITNN equilibrium surrogate enables RL-based stable 400 ms, 1 kHz trajectory control on China's newer HL-3 tokamak.

- **[Regulation Compliant AI for Fusion: Real-Time Image Analysis-Based Control of Divertor Detachment in Tokamaks](https://arxiv.org/abs/2507.02897)** — Chen, Byun, Jalalvand, Kim, Rothstein, Scotti, Allen, Eldon, Erickson & Kolemen, Princeton University / DIII-D National Fusion Facility · *arXiv* · 2025. An interpretable, linear image-based control scheme (not a black-box network) for real-time divertor-detachment feedback control from camera data, reaching 2% mean deviation from target — built explicitly for future regulatory approval of AI fusion controllers.

- **[Magnetic Control of Tokamak Plasmas through Deep Reinforcement Learning](https://www.nature.com/articles/s41586-021-04301-9)** — Degrave et al., DeepMind & EPFL · *Nature* · 2022. The landmark RL plasma control paper. A single RL system autonomously learns to command all control coils of TCV, producing novel "snowflake," "droplet," and ITER-relevant configurations never previously achieved with classical controllers.

- **[Avoiding Fusion Plasma Tearing Instability with Deep Reinforcement Learning](https://www.nature.com/articles/s41586-024-07024-9)** — Seo et al., Princeton/DIII-D · *Nature 626* · 2024. DRL proactively *prevents* tearing instabilities at DIII-D by adjusting plasma shape and NBI power 300ms ahead of instability onset. First real-time avoidance (rather than suppression) of a major disruption cause.

- **[Machine Learning-based Real-time Kinetic Profile Reconstruction in DIII-D](https://iopscience.iop.org/article/10.1088/1741-4326/026006)** — Shousha et al. · *Nuclear Fusion 64* · 2024. NN reconstructs full kinetic profiles in real time from available diagnostics; used as the state input to the DRL tearing mode avoidance controller above.

- **[Alfvén Eigenmode Classification based on ECE Diagnostics at DIII-D using Deep RNNs](https://iopscience.iop.org/article/10.1088/1741-4326/ac3be7)** — Jalalvand et al. · *Nuclear Fusion 62* · 2022. Deep recurrent network classifying Alfvén eigenmodes in real-time from electron cyclotron emission — a key step toward integrated multi-instability control.

- **[Application of ML and AI to Extend EFIT Equilibrium Reconstruction](https://iopscience.iop.org/article/10.1088/1361-6587/ac7186)** — Lao et al. · *Plasma Physics and Controlled Fusion 64* · 2022. ML extending EFIT's real-time equilibrium reconstruction accuracy and coverage; tested at multiple tokamaks.

- **[Feedforward Beta Control in KSTAR by Deep Reinforcement Learning](https://iopscience.iop.org/article/10.1088/1741-4326/ac121a)** — Seo et al. · *Nuclear Fusion 61* · 2021. First DRL control of plasma pressure (β) in KSTAR; foundational work for cross-machine generalization.

- **[Data-driven Profile Prediction for DIII-D](https://iopscience.iop.org/article/10.1088/1741-4326/abdb91)** — Abbate, Conlin & Kolemen · *Nuclear Fusion 61* · 2021. Neural network predicting plasma profiles from operational parameters; enables fast scenario planning between shots.

- **[Machine Learning Control for Disruption and Tearing Mode Avoidance](https://aip.scitation.org/doi/10.1063/1.5125581)** — Fu et al. · *Physics of Plasmas 27* · 2020. Closes the loop between disruption prediction and real-time control response; direct predecessor to the 2024 Nature tearing mode paper.

- **[Fast Modeling of Turbulent Transport Using Neural Networks](https://aip.scitation.org/doi/10.1063/1.5134126)** — van de Plassche et al. · *Physics of Plasmas 27* · 2020. Neural network achieving real-time transport modeling speed, with a **10⁵× speedup** over QuaLiKiz; the widely-cited origin of the modern QuaLiKiz-NN surrogate. See [Turbulence & Transport](#turbulence--transport) for the earlier 2015 precursor.

---

### Disruption Prediction

- **[Balancing Physics Priors and Data for Disruption Prediction in Future Tokamaks](https://iopscience.iop.org/article/10.1088/1741-4326/ae55b7)** — Xue et al., J-TEXT Team, Huazhong University of Science and Technology & ASIPP · *Nuclear Fusion 66* · 2026. "PhyDANet" uses physics-guided domain adaptation to transfer disruption prediction to data-scarce future devices like ITER, showing that explicit physics guidance matters most precisely when target-device data is limited.

- **[Plasma Disruption Prediction on the Nanchang Spherical Tokamak: A Comparative Study of Models Based on Sliding Window Statistical Features](https://link.springer.com/article/10.1007/s10894-026-00590-y)** — Zhang et al. · *Journal of Fusion Energy 45* · 2026. Benchmarks Random Forest, Logistic Regression, SVM and LightGBM on sliding-window statistical features from 201 NCST discharges under a 20 ms warning window; LightGBM reaches 96.7% accuracy and 100% recall.

- **[Hierarchical Multi-to-Single-Modal Knowledge Distillation for Disruption Prediction in EAST](https://arxiv.org/abs/2607.04241)** — Chen et al., ASIPP · *arXiv* · 2026. Distills a multimodal (video + time-series) teacher model into a lightweight time-series-only student, preserving predictive accuracy while cutting inference cost for real-time deployment.

- **[Interpretable Statistical Feature Engineering for Early Disruption Prediction in the Short Pulse ADITYA Tokamak](https://arxiv.org/abs/2608.22515)** — Agarwal, Chaudhury et al., Institute for Plasma Research / DA-IICT, India · *arXiv* · 2026. An interpretable random-forest framework using decision-tree-selected statistical descriptors reaches ROC-AUC 0.87 for early disruption warning on ADITYA, extending disruption ML beyond the usual DIII-D/EAST/JET set to a short-pulse device.

- **[An Interpretable Disruption Predictor on EAST using Improved XGBoost and SHAP](https://iopscience.iop.org/article/10.1088/1741-4326/adeea8)** — Liu et al., Hefei University of Technology & Institute of Plasma Physics CAS · *Nuclear Fusion 65*, 086035 · 2025. A SHAP-explainable XGBoost model predicts EAST disruptions 30 ms ahead with a 96.7% true-positive and 6.58% false-positive rate, identifying vertical displacement and safety factor as key drivers.

- **[DisruptionBench and Complementary New Models: Two Advancements in Machine Learning Driven Disruption Prediction](https://link.springer.com/article/10.1007/s10894-025-00495-2)** — Spangher, Rea et al., MIT PSFC et al. · *Journal of Fusion Energy* · 2025. A standardized cross-machine benchmark spanning Alcator C-Mod, DIII-D and EAST with zero/few/many-shot regimes; introduces a GPT-2-style transformer and a Continuous CNN, the latter reaching 0.97 AUC on C-Mod.

- **[Risk-Aware Framework Development for Disruption Prediction: Alcator C-Mod and DIII-D Survival Analysis](https://doi.org/10.1007/s10894-024-00413-y)** — Keith, Nagpal, Rea & Tinguely, MIT PSFC · *Journal of Fusion Energy 43*, 21 · 2024. Deep Survival Machines applied to disruption prediction, providing calibrated time-to-event estimates and longer warning times compared to binary classifiers.

- **[Disruption Prediction with AI in Tokamak Plasmas](https://www.nature.com/articles/s41567-022-01602-2)** — Vega et al. · *Nature Physics 18* · 2022. Comprehensive review and new results on AI-based disruption warning across JET, AUG, DIII-D; includes lessons and projections for ITER operations.

- **[Disruption Prediction for ITER using a Full Convolutional Neural Network](https://iopscience.iop.org/article/10.1088/1741-4326/abf47d)** — · *Nuclear Fusion* · 2021. FCN applied to multi-diagnostic signal streams; tuned specifically for ITER operational parameters and disruption regimes.

- **[Deep CNNs for Multi-scale Time-series Classification and Disruption Prediction](https://aip.scitation.org/doi/10.1063/5.0006322)** — Churchill et al. · *Physics of Plasmas 27* · 2020. CNNs applied to raw high-temporal-resolution diagnostic data for disruption classification; demonstrates value of working directly with raw signals.

---

### Turbulence & Transport

- **[Machine Learning for Electron-Scale Turbulence Modeling in W7-X](https://arxiv.org/abs/2511.04567)** — Farcas, Fernando, Bañón Navarro, Merlo, Jenko, Max Planck IPP · *Physics of Plasmas 33*, 063903 · 2026. Active-learning-refined regression surrogates predict ETG heat flux at seven W7-X radial locations; finds that a single radius-independent model cannot capture ETG transport, motivating geometry-resolved surrogates for stellarators (versus the tokamak-centric QuaLiKiz-NN paradigm).

- **[Comparison of Neural Network and Gradient-Boosted Decision Tree Surrogates of Linear Gyrokinetic Simulations for Turbulent Transport Modeling in Tokamak Plasmas](https://doi.org/10.1063/5.0304741)** — Lanzarone, Fransson, Camenen, Fuhr, Aix-Marseille Université / CNRS (PIIM) · *Physics of Plasmas 33*, 042302 · 2026. Head-to-head benchmark of gradient-boosted decision trees against neural networks as linear-gyrokinetic surrogates for integrated modeling, informing the choice of ML architecture for the next generation of QuaLiKiz-NN-style transport surrogates.

- **[TGLF-WINN: Data-Efficient Deep Learning Surrogate for Turbulent Transport Modeling in Fusion](https://iopscience.iop.org/article/10.1088/1741-4326/ae72a6)** — Cao, Zhang, Liu, Neiser, Meneghini, Fuller, Smith, Nazikian, Sammuli, Yu, UC San Diego & General Atomics · *Nuclear Fusion 66*, 076031 · 2026. Wavenumber-informed NN surrogate for the TGLF model with physics-guided regularization and Bayesian active learning; matches full-dataset accuracy using 25% of the training data and delivers a 45× speedup in flux-matching workflows.

- **[GKFieldFlow: A Spatio-Temporal Neural Surrogate for Nonlinear Gyrokinetic Turbulence](https://arxiv.org/abs/2601.02614)** — Ashourvan, PPPL · *arXiv* · 2026. A 3D U-Net + temporal convolutional network trained directly on nonlinear CGYRO field data, jointly forecasting evolving turbulent potential fields and ion/electron/particle fluxes autoregressively — going beyond flux-only surrogates to reproduce the underlying turbulence dynamics.

- **[GyroSwin: 5D Surrogates for Gyrokinetic Plasma Turbulence Simulations](https://arxiv.org/abs/2510.07314)** — Paischer, Galletti et al., JKU Linz & UKAEA Culham · *NeurIPS 2025* · 2025. First scalable neural surrogate for the full 5D nonlinear gyrokinetic equation (not a reduced quasilinear model), extending hierarchical Vision Transformers to 5D with cross-attention between the distribution function and electrostatic potential; cuts nonlinear gyrokinetic simulation cost by three orders of magnitude and scales to 1B parameters.

- **[Efficient Dataset Construction using Active Learning and Uncertainty-Aware Neural Networks for Plasma Turbulent Transport Surrogate Models](https://arxiv.org/abs/2507.15976)** — Ho, Zanisi, de Leeuw, Galvan, Rodriguez-Fernandez, Howard et al., MIT PSFC & UKAEA · *Physics of Plasmas 32*, 093903 · 2025. Uses uncertainty-aware architectures (SNGP, BNN-NCP) with QuaLiKiz as an in-the-loop labeller to build turbulent-transport training sets far smaller than brute-force sampling, reaching ~0.75 R² across multiple turbulent modes and fluxes.

- **[AI-Accelerated CGYRO for ITER Baseline Scenario Verification](https://news.mit.edu/2025/unlocking-secrets-fusions-core-ai-enhanced-simulations-0218)** — Howard et al., MIT PSFC · 2025. AI surrogates of the CGYRO gyrokinetic code verify and optimize the ITER baseline plasma scenario, with outputs informing actual ITER operating point selection.

- **[Multi-Fidelity Surrogate for Plasma Turbulence via Transfer Learning](https://journals.aps.org/pre/abstract/10.1103/PhysRevE.111.L013202)** — Wan et al. · *Physical Review E* · 2025. See [Generative AI section](#generative-ai--diffusion-models). Transfer learning paradigm for turbulence emulation at high fidelity with minimal expensive samples.

- **[Machine Learning for Turbulent Structure Tracking with Ultra-Fast Imaging](https://www.nature.com/articles/s41598-024-79251-z)** — · *Scientific Reports* · 2024. YOLO + semantic segmentation for real-time detection and tracking of plasma filaments (blobs) from fast camera data; overcomes human subjectivity and bottleneck in turbulence characterization.

- **[Physics-Informed Neural Networks for Turbulent Heat Transport](https://arxiv.org/abs/2104.01444)** — · *arXiv* · 2021. PINNs embedding turbulent heat transport equations; preserves physical conservation laws by construction rather than as a soft regularizer.

- **[Real-time Capable First Principle Based Modelling of Tokamak Turbulent Transport](https://iopscience.iop.org/article/10.1088/0029-5515/55/9/092001)** — Citrin, Breton, Felici, Imbeaux, Aniel, Artaud, Baiocchi, Bourdelle, Camenen, Garcia · *Nuclear Fusion 55*, 092001 (arXiv: [1502.07402](https://arxiv.org/abs/1502.07402)) · 2015. The original neural-network surrogate of QuaLiKiz demonstrating real-time-capable transport modeling; the precursor to van de Plassche et al.'s 2020 QuaLiKiz-NN (see [Plasma Control & RL](#plasma-control--reinforcement-learning)), which is the version now widely adopted across integrated modeling workflows.

---

### Surrogate Models & Emulators

- **[Millisecond-Scale Neural Operator Surrogates for Double-Null Free-Boundary Grad–Shafranov Equilibria](https://arxiv.org/abs/2608.05555)** — Krastev, Harvard University · *arXiv* · 2026. A Fourier Neural Operator maps operating parameters and X-point locations directly to poloidal-flux equilibria at 0.05% mean relative L² error and ~640× the speed of the FreeGS solver, recovering X-points to 0.2 cm accuracy for real-time optimization and control workflows.

- **[Experimental Validation of a Fast Control-Oriented, Physics-Informed Surrogate Model for Plasma Equilibrium Reconstruction in the TCV Tokamak](https://arxiv.org/abs/2606.09487)** — Grandin, Mele, Galperti, Gonzales Castiñeiras, Heiß, Cenedese, EPFL Swiss Plasma Center & EUROfusion · *arXiv* · 2026. Physics-informed neural surrogate for LIUQE-class equilibrium reconstruction, trained on ~10,000 discharges, achieving sub-100-microsecond inference for 10 kHz shape control — deployed live on TCV's real-time control system, not just tested offline. See [Digital Twins](#digital-twins--simulation-acceleration).

- **[A Novel Numerical Algorithms Optimization Method with Machine Learning Frameworks: Real-Time Plasma Equilibrium Reconstruction in EXL-50U Spherical Torus](https://arxiv.org/abs/2601.12378)** — Zheng, Liu, Gu, Zhang, Li et al., EXL-50U Team · *arXiv* · 2026. PyTorch/TensorRT-accelerated real-time Grad–Shafranov solver ("PTEFIT") reaching 0.268 ms per time slice, used for live plasma-position and isoflux feedback control on the EXL-50U spherical torus.

- **[Learning Collision Operators from Plasma Phase-Space Data using Differentiable Simulators](https://arxiv.org/abs/2601.10885)** — Carvalho, Bilbao, Mori, Silva, Alves, IST Lisbon (GoLP) & UCLA · *Journal of Plasma Physics* · 2026. A differentiable kinetic simulator learns collision operators directly from PIC phase-space data instead of assuming a closed analytic form, outperforming particle-track estimators — a data-driven complement to Fokker–Planck–Landau surrogates like FPL-net.

- **[Surrogate Models for Nuclear Fusion with Parametric Shallow Recurrent Decoder Networks: Applications to Magnetohydrodynamics](https://arxiv.org/abs/2603.10678)** — Lo Verso, Introini, Cervi, Savoldi, Kutz, Cammi, Politecnico di Milano & University of Washington · *arXiv* · 2026. A shallow recurrent decoder network reconstructs full lead–lithium breeding-blanket MHD velocity/pressure/temperature fields from just three point sensors, generalizing to magnetic field strengths unseen in training — aimed at real-time blanket monitoring.

- **[FPL-net: Deep Learning for the Nonlinear Fokker–Planck–Landau Collision Operator](https://doi.org/10.1016/j.jcp.2024.113665)** — Lee & Yoon, UNIST · *Journal of Computational Physics* · 2024. CNN encoder-decoder achieving **1,000× speedup** over CPU-based codes for plasma collision physics; cornerstone component for real-time digital twins of fusion reactors.

- **[Real-time Reservoir Computing with Application to Profile Prediction in Fusion Plasma](https://ieeexplore.ieee.org/document/9490338)** — Jalalvand et al. · *IEEE Transactions on Neural Networks and Learning Systems* · 2022. Reservoir computing for real-time and adaptive plasma profile prediction; low memory footprint suitable for embedded control systems.

- **[Accelerated Version of NUBEAM Capabilities on DIII-D Using Neural Networks](https://www.sciencedirect.com/science/article/pii/S0920379620308248)** — Morosohk, Boyer & Schuster · *Fusion Engineering and Design* · 2021. Neural surrogate for the NUBEAM neutral beam injection code, enabling real-time NBI fast-ion calculations.

- **[Deep Neural Network Grad-Shafranov Solver Constrained with Magnetic Signals](https://iopscience.iop.org/article/10.1088/1741-4326/ab1f28)** — Joung et al. · *Nuclear Fusion* · 2020. NN-based equilibrium solver constrained by real measured magnetic signals; faster than iterative Grad-Shafranov solvers while respecting physics constraints.

---

### Neutronics & Materials

- **[Efficient and Accurate Spatial Mixing of Machine Learned Interatomic Potentials for Materials Science](https://www.nature.com/articles/s41524-026-01982-6)** — Birks, Nutter, Swinburne & Kermode, University of Warwick / Aix-Marseille Université · *npj Computational Materials* · 2026. Introduces ML-MIX, a package that spatially blends cheap and expensive ML potentials for up to 11× speedups; validated on helium implantation into tungsten, a key plasma-facing-material damage mechanism.

- **[Machine Learning Accelerates Analysis of Fusion Materials](https://www.ornl.gov/news/machine-learning-accelerates-analysis-fusion-materials-0)** — Juneja & Unterberg, Oak Ridge National Laboratory · ORNL News · 2026. A generative ML model trained on 3,200 SEM images of irradiated tungsten synthesizes realistic novel micrographs (cracks, pores, microstructure), enabling "virtual experiments" that augment scarce plasma-facing-component damage data.

- **[Nine-Element Machine-Learned Interatomic Potentials for Multiphase Refractory Alloys](https://arxiv.org/abs/2603.04147)** — Byggmästar, Lopes, Fan & Ala-Nissila, University of Helsinki / Aalto University · *arXiv* · 2026. MLIPs (tabGAP and NEP) spanning nine refractory elements (Ti, Zr, Hf, V, Nb, Ta, Cr, Mo, W), applied to radiation-damage cascade simulation in a WTaCrVHf metallic glass — relevant to fusion structural/first-wall alloy design.

- **[DuctGPT: A Generative Transformer for Forward Screening of Ductile Refractory Multi-Principal Element Alloys](https://www.sciencedirect.com/science/article/abs/pii/S135964542501050X)** — Guduru, Kekung, Ott, Roy & Singh, Ames National Laboratory · *Acta Materialia 306* · 2025–2026. A GPT-style generative model (fine-tuned from NIST's AtomGPT) screens refractory multi-principal-element alloys for high-temperature strength and ductility on a desktop in seconds, cutting fusion alloy discovery from months to hours.

- **[Machine Learning Interatomic Potentials for Fusion Materials](https://www.sciencedirect.com/science/article/pii/S0022311521005560)** — · *Journal of Nuclear Materials* · 2021. MLIP for tungsten and first-wall plasma-facing materials under neutron irradiation; enables MD simulations at near-DFT accuracy at orders-of-magnitude larger scale and timescale.

- **[Active Learning for Fusion-Relevant Materials Discovery](https://www.nature.com/articles/s41524-022-00805-8)** — · *npj Computational Materials* · 2022. Bayesian active learning accelerating high-entropy alloy screening for plasma-facing components; reduces required DFT calculations by ~80%.

- **[ML-Based Compton Suppression for Fusion Plasma Gamma Diagnostics](https://arxiv.org/abs/2312.13685)** — Lennon et al. · *arXiv* · 2023. ML pulse-shape discrimination for HPGe detectors improving fusion neutron diagnostic sensitivity by 51% on Am-241 MDA — directly enabling more accurate fusion power measurements.

- **[Graph Neural Networks for Radiation Damage Prediction](https://arxiv.org/abs/2106.09322)** — · *arXiv* · 2021. GNNs predicting cascade damage distributions in structural materials from atomistic simulation inputs; faster than classical molecular dynamics for damage screening.

- **[Optimization and Supervised ML for Fitting Numerical Fusion Physics Models](https://iopscience.iop.org/article/10.1088/1361-6471/abd009)** — Bollapragada et al. · *Journal of Physics G* · 2021. Derivative-free optimization combined with ML for fitting complex nuclear physics models relevant to fusion blanket and materials design.

---

### Diagnostics & Sensing

- **[TokaMind](https://arxiv.org/abs/2602.15084) & [FusionMAE](https://arxiv.org/abs/2509.12945)** — 2025–2026. See [LLMs & Foundation Models](#llms--foundation-models). The first large-scale multimodal/masked-autoencoder foundation models trained specifically on tokamak diagnostic data (MAST and HL-3 respectively), enabling virtual-diagnostic reconstruction and cross-task transfer.

- **[Regulation Compliant AI for Fusion: Real-Time Image Analysis-Based Control of Divertor Detachment in Tokamaks](https://arxiv.org/abs/2507.02897)** — Chen, Kolemen et al., Princeton University & PPPL · *arXiv* · 2025. See [Plasma Control & RL](#plasma-control--reinforcement-learning). Interpretable, camera-based AI feedback for divertor detachment, designed explicitly for regulatory/explainability requirements.

- **[AI Foundation Models for Experimental Fusion Diagnostics](https://www.frontiersin.org/journals/physics/articles/10.3389/fphy.2024.1531334/full)** — Churchill, PPPL · *Frontiers in Physics* · 2025. See [LLMs & Foundation Models](#llms--foundation-models). Full treatment of foundation model architectures for multi-diagnostic fusion data.

- **[Multimodal super-resolution: discovering hidden physics and its application to fusion plasmas](https://www.nature.com/articles/s41467-025-63492-1)** — Jalalvand, Kim, Seo, Hu, Curie, Steiner, Nelson, Na & Kolemen, Princeton University / PPPL / Chung-Ang University / Columbia / Seoul National University · *Nature Communications* · 2025. Multimodal transformer fusing heterogeneous DIII-D diagnostic streams to super-resolve plasma state; reveals magnetic-island ELM-suppression dynamics invisible to any single instrument.

- **[Application of ML for Detecting Turbulent Structures via Ultra-Fast Imaging](https://www.nature.com/articles/s41598-024-79251-z)** — · *Scientific Reports* · 2024. YOLO-based real-time detection and tracking of plasma filaments from fast cameras; replaces slow, subjective manual analysis.

- **[ML-Based Real-time Kinetic Profile Reconstruction in DIII-D](https://iopscience.iop.org/article/10.1088/1741-4326/026006)** — Shousha et al. · *Nuclear Fusion 64* · 2024. Real-time NN reconstruction of kinetic profiles; used as the state vector for the DRL tearing mode controller.

- **[Bolometry Tomography with Deep Learning on JET](https://iopscience.iop.org/article/10.1088/1741-4326/ab24b4)** — · *Nuclear Fusion* · 2020. CNN-based tomographic inversion for plasma emission imaging; replaces classical SART/MFI iterative methods with a millisecond-scale forward pass.

---

### Inertial Confinement Fusion (ICF)

- **[Co4ICF: Co-evolving Physics-Informed Surrogate and RL-based Pulse Optimizer for Inertial Confinement Fusion](https://arxiv.org/abs/2607.10366)** — Zhao, Zhang, Wang, Wu & Yan · *Proceedings of ACM SIGKDD 2026 (KDD '26)* · 2026. A PPO-based pulse optimizer co-evolves with its own surrogate model to correct out-of-distribution extrapolation errors during optimization, reaching 146% normalized yield in 1D and generalizing (246.9%) to unseen 2D physics without retraining.

- **[High-Dimensional Inverse Design of Inertial Fusion Implosions via Differentiable Simulation](https://arxiv.org/abs/2606.08827)** — Crilly, Travis, Brodrick, Coughlin & Joglekar, Imperial College London (Centre for Inertial Fusion Studies) · *arXiv* · 2026. Uses automatic differentiation through a radiation-hydrodynamics model (not a black-box surrogate) to gradient-optimize 500-parameter laser pulses for OMEGA-scale direct-drive implosions, recovering optimal pulse shapes without hand-set constraints.

- **[Automated Simulation-Based Design via Multi-Fidelity Active Learning and Optimisation for Laser Direct Drive Implosions](https://pubs.aip.org/aip/pop/article/33/1/012702/3376425/Automated-simulation-based-design-via-multi)** — Crilly, Moloney, Shi & Ferdinandi, Imperial College London · *Physics of Plasmas 33*, 012702 · 2026. Combines 1D/2D neural-network surrogates with Bayesian active learning to find hydrodynamic-instability-resistant direct-drive designs at 25 kJ scale, then validates the scaling to a 2 MJ reactor-relevant design including alpha-heating.

- **[Causal Multi-Fidelity Surrogate Forward and Inverse Models for ICF Implosions](https://www.nature.com/articles/s41598-026-57115-y)** — Maltba, Southworth, Haack & Klasky, Los Alamos National Laboratory · *Scientific Reports* · 2026. A causal, controller-in-the-loop reduced-order surrogate maps time-dependent radiation drive to DT-interface dynamics, then solves inverse design/diagnostic problems orders of magnitude faster than full radiation-hydrodynamics codes.

- **[Predicting Fusion Ignition at the National Ignition Facility with Physics-Informed Deep Learning](https://www.science.org/doi/10.1126/science.adm8201)** — Spears, Humbird, Brandon, Casey, Field, Gaffney et al., Lawrence Livermore National Laboratory · *Science 389*, Issue 6761 · 2025. A physics-informed deep-learning surrogate trained on 150,000+ simulations plus experimental history predicted a >70% ignition probability for the historic December 2022 NIF shot, with the actual yield falling inside the predicted range.

- **[Multi-Agent Design Assistant for the Simulation of Inertial Fusion Energy (MADA)](https://arxiv.org/abs/2510.17830)** — LLNL / Sandia / LANL · *arXiv* · 2025. See [AI Agents](#ai-agents--autonomous-experiment-design). Full agentic LLM system driving HPC ICF simulation campaigns autonomously.

- **[LPI-LLM: ICF Forecasting via Large Language Models](https://arxiv.org/abs/2407.11098)** — · *ICLR 2025 submission* · 2024. See [LLMs & Foundation Models](#llms--foundation-models). LLMs + reservoir computing for LPI dynamics with the LPI4AI benchmark.

- **[Machine Learning Optimizes High-Power Laser Experiments at NIF](https://lasers.llnl.gov/news/machine-learning-optimizes-high-power-laser-experiments)** — LLNL/NIF · 2024. ML-driven shot parameter optimization producing measurable ICF implosion performance improvements after NIF's historic ignition milestone.

- **[Machine Learning for ICF Implosion Design](https://www.sciencedirect.com/science/article/pii/S2589004222007313)** — · *iScience* · 2022. Gaussian processes and Bayesian optimization for NIF target geometry and laser pulse design; precursor approach to the MADA agentic system.

- **[Neural Network Surrogates for ICF Hydrodynamic Simulations](https://arxiv.org/abs/2006.04806)** — · *arXiv* · 2020. Emulating HYDRA-class radiation-hydrodynamics codes with deep networks; integrated into the MADA design workflow.

---

### Digital Twins & Simulation Acceleration

- **[iGENE: A Differentiable Flux-Tube Gyrokinetic Code in TensorFlow](https://arxiv.org/abs/2605.03086)** — Artigues, Merlo & Jenko · *Physics of Plasmas* · 2026. Fully differentiable TensorFlow reimplementation of the electromagnetic local nonlinear gyrokinetic model, opening gyrokinetic turbulence codes directly to gradient-based optimization, uncertainty quantification, and profile-prediction workflows.

- **[AI Surrogate Modeling for Real-Time Tokamak Equilibrium Prediction: Benchmarking Neural Architectures and Validation on EXL-50U](https://arxiv.org/abs/2608.23217)** — Shi, Zhang, Ding et al. · *arXiv* · 2026. Benchmarks MLP, CNN, FNO, Transformer and KAN surrogates on a 100,000-sample Grad-Shafranov database; CNN reaches 0.7 ms TensorRT latency with the best accuracy/robustness/speed balance, validated on the real EXL-50U spherical tokamak.

- **[Accelerating Integrated Modeling with Surrogate-Based Optimization: The MAESTRO Workflow](https://arxiv.org/abs/2605.07047)** — Rodriguez-Fernandez, Howard et al., MIT Plasma Science and Fusion Center · *arXiv* (submitted to *Plasma Physics and Controlled Fusion*) · 2026. Couples the PORTALS surrogate-based transport-optimization framework to external equilibrium, pedestal, divertor and heating solvers, enabling fast full-physics steady-state plasma-profile predictions for digital-twin-style integrated tokamak modeling.

- **[Experimental Validation of a Fast Control-Oriented, Physics-Informed Surrogate Model for Plasma Equilibrium Reconstruction in the TCV Tokamak](https://arxiv.org/abs/2606.09487)** — Grandin, Mele, Galperti, Heiß, Cenedese et al., EPFL Swiss Plasma Center / EUROfusion · *arXiv* · 2026. See [Surrogate Models](#surrogate-models--emulators). Sub-100-microsecond equilibrium surrogate deployed live on TCV's real-time control system for 10 kHz shape control.

- **[PPPL Launches STELLAR-AI Platform to Accelerate Fusion Energy Research](https://www.pppl.gov/news/2026/pppl-launches-stellar-ai-platform-accelerate-fusion-energy-research)** — PPPL + DOE Genesis Mission partners · 2026. See [AI Agents](#ai-agents--autonomous-experiment-design). AI+HPC platform building digital-twin models of NSTX-U and connecting compute directly to the live experiment.

- **[NVIDIA and General Atomics Advance Commercial Fusion Energy](https://blogs.nvidia.com/blog/nvidia-general-atomics-fusion/)** — NVIDIA & General Atomics, with Argonne Leadership Computing Facility and NERSC · 2025. Interactive AI-enabled digital twin of the DIII-D National Fusion Facility built in NVIDIA Omniverse, fusing live sensor data, physics simulations, engineering models and three trained AI surrogates (EFIT for equilibrium, CAKE for plasma boundary, ION ORB for escaping-ion heat load) into one synchronized environment. Cuts plasma-behavior prediction from weeks to seconds; used by ~700 scientists across 100 organizations for "what-if" reactor-design and operating-scenario testing.

- **[TORAX: A Differentiable JAX-based Tokamak Transport Simulator](https://github.com/google-deepmind/torax)** — DeepMind · *open-sourced* · 2024. GPU-acceleratable, fully differentiable plasma core transport simulator built for RL training and gradient-based optimization. Enables millions of virtual SPARC shots before the real machine fires; core tool of the DeepMind × CFS collaboration.

- **[FPL-net: 1,000× Speedup for Fokker–Planck–Landau Collision Operator](https://doi.org/10.1016/j.jcp.2024.113665)** — Lee & Yoon · *Journal of Computational Physics* · 2024. See [Surrogate Models](#surrogate-models--emulators). Cornerstone for real-time plasma physics digital twins.

- **[AI-Coupled CGYRO for ITER Baseline Scenario Verification](https://news.mit.edu/2025/unlocking-secrets-fusions-core-ai-enhanced-simulations-0218)** — MIT PSFC · 2025. AI surrogates dramatically accelerate CGYRO gyrokinetic code, validating the ITER baseline operating point with turnaround times compatible with machine operations.

---

### Reactor Design Optimization

- **[Towards Joint Optimization of Stellarator Coils and Support Structures](https://arxiv.org/abs/2607.05749)** — Fu & Kaptanoglu, NYU Courant Institute · *arXiv* · 2026. Open-source "coil-fem" tool couples differentiable finite-element structural analysis with coil-shape optimization, jointly optimizing coil geometry and support-clamp placement — the first published combined coil+support co-optimization, achieving 2.4× lower RMS von Mises stress at similar field error versus an unoptimized baseline.

- **[A Proof-of-Concept for Automated AI-Driven Stellarator Coil Optimization with In-the-Loop Finite-Element Calculations](https://arxiv.org/abs/2603.15240)** — Kaptanoglu (NYU Courant) & Gil (Max Planck Institute for Plasma Physics) · *arXiv* · 2026. Fully automated coil-design pipeline offering a choice of genetic-algorithm or LLM-driven search, with in-the-loop finite-element Von Mises stress calculations feeding back into the optimization loop, results published to a public leaderboard.

- **[Bayesian Optimization of Stellarator Alpha-Particle Confinement using Data-Informed Parameter Spaces and Dimensionality Reduction](https://arxiv.org/abs/2606.19523)** — Landreman (U. Maryland) et al., with Cornell and Flatiron Institute co-authors · *arXiv* · 2026. Introduces bounded, data-informed parameterizations that make Bayesian optimization of fast-particle confinement tractable with guiding-center tracing inside the loop, producing configurations with strong alpha-particle confinement even far from quasisymmetry/QI.

- **[Accelerating the Engineering Design of Breeder Blankets with Parametric Optimisation and Sequential Learning](https://doi.org/10.3389/fnuen.2025.1694684)** — Humphrey, Brooks, Mungale, Davis & Foster, UK Atomic Energy Authority · *Frontiers in Nuclear Engineering* · 2026. Couples parametric geometry, OpenMC neutronics, MOOSE thermal-hydraulics and Bayesian sequential-learning optimization to raise a solid breeder blanket's tritium breeding ratio (0.723→0.802) and a combined performance figure of merit (1.68→2.04) — a rare example of full engineering + neutronics AI-driven blanket design.

- **[Data-Driven Generation of Compact Quasi-Isodynamic Stellarators](https://arxiv.org/abs/2608.16938)** — Han et al., ASIPP / USTC · *arXiv* · 2026. See [Generative AI](#generative-ai--diffusion-models). Conditional generative model extending ConStellaration-style boundary generation to ultra-compact QI stellarators.

- **[ConStellaration: A Dataset of QI-like Stellarator Plasma Boundaries and Optimization Benchmarks](https://arxiv.org/abs/2506.19583)** — Cadena et al., Proxima Fusion, in collaboration with Hugging Face · *NeurIPS 2025* · 2025. Open dataset of ~158,000 QI-like stellarator boundaries with VMEC++ MHD equilibria, plus three optimization benchmarks of increasing complexity (geometric, "simple-to-build," multi-objective stability); underpins the public Proxima Fusion × Hugging Face challenge and multiple 2026 follow-on papers. See [Datasets](#-datasets).

- **[Design Optimization of Nuclear Fusion Reactor through Deep Reinforcement Learning](https://arxiv.org/abs/2409.08231)** — · *arXiv* · 2024. DRL agent explores multi-physics tokamak reactor design space (plasma, engineering, neutronics constraints) autonomously, discovering novel operating regimes inaccessible to grid search.

- **[Diffusion for Fusion: Designing Stellarators with Generative AI](https://arxiv.org/abs/2511.20445)** — Padidar et al. · *arXiv* · 2025. See [Generative AI](#generative-ai--diffusion-models). Conditional diffusion model for stellarator coil inverse design.

- **[Omnigenous Stellarator Equilibria with Enhanced Stability](https://arxiv.org/abs/2410.04576)** — Gaur, Conlin, Dickinson, Parisi, Dudt, Panici, Kim, Unalmis, Dorland & Kolemen · *arXiv* · 2024. Uses the GPU-accelerated, differentiable DESC optimization suite to search omnigenous configuration space for Mercier/ideal-ballooning/kinetic-ballooning stability, yielding stellarator designs with improved confinement beyond classical optimization.

---

### Reviews & Roadmaps

- **[Challenges and Opportunities for AI to Help Deliver Fusion Energy](https://iopscience.iop.org/article/10.1088/1361-6587/ae775c)** — Agnello, Brooks, Cowley, Georgescu, Higginbottom, Pearson, Shears, Windridge · *Plasma Physics and Controlled Fusion 68*, 063701 · 2026. Perspective from a UKAEA/STFC/industry/academia roundtable arguing AI has real potential in fusion but needs responsible methodology and sustained fusion–AI collaboration; explicitly cautions that not every fusion problem is best solved with AI.

- **[A Review of Machine Learning-Driven Studies of Tearing Modes in Tokamaks](https://pubs.aip.org/aip/pop/article/33/5/050501/3391098/A-review-of-machine-learning-driven-studies-of)** — Rea & Benjamin · *Physics of Plasmas 33*, 050501 · 2026. Comprehensive review of a decade of ML applied to tearing-mode prediction and control across tokamaks, complementing the tearing-mode interpretability paper below.

- **[The IAEA Fusion Data Lake Project — Accelerating AI and Big Data Applications through Open Science and FAIR Data](https://arxiv.org/abs/2604.01797)** — Gahle & Barbarino, IAEA · *arXiv* (Sixth IAEA Technical Meeting on Fusion Data Processing) · 2026. Roadmap for an international fusion data infrastructure (catalogue, centralized storage, federation across 24 institutions/11 countries) explicitly built to enable AI/ML applications; proof-of-concept integrates UKAEA's MAST Data Catalog.

- **[How Fusion Is Teaching AI New Tricks at ITER](https://www.iter.org/node/20687/how-fusion-teaching-ai-new-tricks-iter)** — ITER Organization · *ITER Newsline* · 2026. Survey of AI initiatives across ITER: an internal LLM assistant for engineering-record retrieval, a planned "fusion world model" trained across existing tokamaks to predict machine behavior, digital twins, and millisecond surrogate models.

- **[Application and Prospects of Big Data and AI in Magnetic Confinement Fusion](https://www.sciopen.com/article/10.16791/j.cnki.sjg.2025.04.001)** — Zhang et al. · *Experimental Technology and Management* · 2025. Comprehensive review of AI integration across the full MCF research pipeline — simulation, diagnostics, control, and materials.

- **[Interpreting AI for Fusion: Application to Plasma Profile Analysis for Tearing Mode Stability](https://arxiv.org/abs/2502.20294)** — · *arXiv* · 2025. Shapley-value-based interpretability framework for fusion ML models; bridges the gap between opaque ML predictions and actionable physics understanding for tearing mode control.

- **[Machine Learning and Bayesian Methods in Fusion: A Review](https://arxiv.org/abs/2301.11234)** — Pavone et al. · *arXiv* · 2023. Comprehensive review of Bayesian and ML methods in fusion — disruption prediction, surrogates, diagnostics, Bayesian inference, and control. Extensive citation index useful as a literature map.

- **[Advancing Fusion with Machine Learning: Research Needs Workshop Report](https://link.springer.com/article/10.1007/s10894-020-00258-1)** — Humphreys et al. · *Journal of Fusion Energy* · 2020. The seminal DOE-sponsored ML roadmap for fusion; defines five Priority Research Opportunities (PROs) still guiding funding and research agendas.

---

## 📊 Datasets

| Dataset | Device | Contents | Access |
|---|---|---|---|
| [ConStellaration](https://github.com/proximafusion/constellaration) | Stellarator | ~158,000 QI-like stellarator plasma boundaries paired with ideal-MHD equilibria (VMEC++) and performance metrics; 3 optimization benchmarks of increasing difficulty | Public ([HF dataset](https://huggingface.co/datasets/proxima-fusion/constellaration)) |
| [FAIR-MAST](https://github.com/ukaea/fair-mast) | MAST / MAST-U | Full experimental tokamak dataset (11,573+ shots, 39 diagnostic signal categories) via public catalog, S3 (parquet/zarr), REST/GraphQL API | Public ([mastapp.site](https://mastapp.site/)) |
| [TokaMark Benchmark](https://github.com/UKAEA-IBM-STFC-Fusion-FMs/tokamark_baseline) | MAST | Curated 14-task benchmark (time-series, 2D profiles, video) on real MAST experiments/diagnostics for evaluating fusion foundation models; companion to TokaMind | Public, CC BY 4.0 |
| [Fusion Equilibrium Challenge Dataset](https://huggingface.co/datasets/Sophelio/fusion-equilibrium-challenge) | DIII-D + MAST | ~9,100 curated shots (7,915 DIII-D + 1,206 MAST), harmonized schema; poloidal-field coil currents + Thomson profiles for magnetic-geometry inference without magnetic diagnostics; NeurIPS 2026 competition dataset | Public, CC BY 4.0 |
| [ITER IMAS](https://imas.iter.org/) | ITER / multi-device | Standardized plasma data schema (OMAS-compatible) — the emerging universal standard | Registered |
| [JET Pulse Data (EUROfusion)](https://www.euro-fusion.org/fusion-database/) | JET | Full pulse diagnostics, disruption shots, D-T campaign data | Application |
| [DIII-D Data Archive](https://d3dfusion.org/) | DIII-D | Shots, equilibrium, kinetic profiles, NBI data; ~500 TB of research data, now linked to an NVIDIA Omniverse digital twin (2025) | Public (via user agreement) |
| [EAST Open Data](https://lssf.cas.cn/en/facilities/energy/east/dr/) | EAST | Disruption database, multi-channel diagnostic signals, via the CAS Large Research Infrastructures data-resource portal | Public |
| [Alcator C-Mod Data (MDSplus Archive)](https://cmodwiki.psfc.mit.edu/index.php/MDSplus) | C-Mod | Disruption database, Thomson scattering profiles; ~51,000 shots preserved post-decommissioning (135 TB) | Public |
| [KSTAR Dataset](https://www.kfe.re.kr) | KSTAR | Operation data, H-mode shots, ELM classification labels, via the Korea Institute of Fusion Energy (the direct KSTAR data subdomain can be unreachable outside Korea's network) | Registered |
| [QUASR: Quasisymmetric Stellarator Database](https://quasr.flatironinstitute.org/) | — | Optimized stellarator coils and magnetic surfaces; training set for "Diffusion for Fusion" (2025) | Public |
| [LPI4AI](https://arxiv.org/abs/2407.11098) | NIF-class ICF | 40,000 Laser-Plasma Instability samples from 100 experimental shot sequences; first LPI ML benchmark | On release |
| [NIF Shot Archive](https://nifuserguide.llnl.gov/home/8-data-handling) | NIF | Facility data-handling system (300M+ archive objects, 4,000+ experiments) documented in the NIF User Guide; not an openly downloadable dataset | Restricted (NIF users) |
| [OpenADAS](https://open.adas.ac.uk/) | — | Atomic data for plasma modeling: rate coefficients, cross-sections, spectral data | Public |
| [IAEA Nuclear Data Services](https://www-nds.iaea.org/) | — | AME2020 atomic masses, neutron cross-sections, decay data | Public |

---

## 🛠️ Tools & Libraries

| Tool | Description | Language |
|---|---|---|
| [VMEC++](https://github.com/proximafusion/vmecpp) | Python-friendly, from-scratch C++ reimplementation of VMEC (free-boundary ideal-MHD stellarator/tokamak equilibrium solver) by Proxima Fusion; PyPI package, SIMSOPT-compatible, hot-restart support; used to generate the ConStellaration dataset | C++/Python |
| [FreeGSNKE](https://github.com/FusionComputingLab/freegsnke) | Evolutive free-boundary tokamak equilibrium simulation for plasma scenario design, control analysis, and virtual-circuit optimization; STFC Hartree Centre / UKAEA, validated on MAST-U | Python |
| [TORAX](https://github.com/google-deepmind/torax) | Differentiable JAX tokamak core transport simulator (DeepMind, 2024); designed for RL training and gradient-based scenario optimization; backbone of the DeepMind × CFS/SPARC collaboration | Python/JAX |
| [DESC](https://github.com/PlasmaControl/DESC) | Differentiable stellarator equilibrium solver and coil optimizer (JAX); used in stellarator generative AI and inverse design work | Python/JAX |
| [QuaLiKiz-NN (QLKNN-fortran)](https://gitlab.com/qualikiz-group/QLKNN-fortran) | Neural network surrogate of the QuaLiKiz gyrokinetic transport code; 10⁵× faster than the original; integrated into integrated modeling workflows (development code: [QLKNN-develop](https://gitlab.com/qualikiz-group/QLKNN-develop)) | Python/Fortran |
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
| [GKX](https://github.com/uwplasma/GKX) | Gyrokinetic flux-tube turbulence (tokamak & stellarator) | JAX-native, fully differentiable linear/nonlinear gyrokinetics (2026); plugs directly into VMEC-based stellarator optimization loops |
| [gyaradax](https://github.com/gerkone/gyaradax) | Local (flux-tube) gyrokinetics | JAX/GPU rewrite of GKW with autodiff; ~10.5× speedup enabling gradient-based inverse design (arXiv:2604.06085, 2026) |
| [iGENE](https://arxiv.org/abs/2605.03086) | Electromagnetic local nonlinear gyrokinetics | Fully differentiable TensorFlow reimplementation of GENE; opens gyrokinetic turbulence codes to gradient-based optimization and UQ (2026) |
| [TORAX](https://github.com/google-deepmind/torax) | 1D plasma core transport | DeepMind (2024); JAX-based, differentiable, GPU-ready; backbone of SPARC AI pilot |
| [GENE](http://genecode.org/) | Gyrokinetic turbulence (flux-tube & global) | Active surrogate model coupling work; used in QuaLiKiz-NN training data generation |
| [GS2](https://gyrokinetics.gitlab.io/gs2/) | Gyrokinetic turbulence | Open-source; Python wrappers available; used in ML transport surrogates |
| [CGYRO](https://gafusion.github.io/doc/cgyro.html) | Global gyrokinetics | General Atomics; targeted by MIT AI surrogate work for ITER baseline verification (2025) |
| [XGC](https://hbps.pppl.gov/computing/xgc-1) | Total-f global gyrokinetics | Exascale code; ML coupling workflows developed at ORNL |
| [SOLPS-ITER](https://www.iter.org/node/20687/iter-unveils-new-tool-plasma-edge-modelling-solps-iter) | Scrape-off-layer plasma & neutral transport | ITER standard edge code, being incorporated into the IMAS modeling suite; docs at [solps-tutorials.readthedocs.io](https://solps-tutorials.readthedocs.io/) |
| [BOUT++](https://boutproject.github.io/) | 3D fluid plasma turbulence | Open-source; Python interface; active ML surrogate development |
| [MARBL](https://computing.llnl.gov/projects/mapp) | 3D radiation-hydrodynamics | LLNL next-gen multiphysics ICF/HED code, developed under the MAPP project; targeted by MADA LLM agents (2025) |
| [HYDRA](https://sd.llnl.gov/stockpile-science/high-performance-computing/proprietary-software) | Radiation-hydrodynamics | LLNL; NIF ICF standard code, distributed to DOE collaborators; surrogated in ML ICF design papers |
| [OpenMC](https://openmc.org/) | Monte Carlo neutron/photon transport | Open-source; Python API; used in ML-coupled blanket neutronics design |

---

> **Contributing:** PRs welcome! Please include the paper DOI or arXiv link, year, venue, and a one-sentence note on why it's notable. See [CONTRIBUTING.md](CONTRIBUTING.md).
