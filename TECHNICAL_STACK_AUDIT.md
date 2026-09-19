# Technical Stack & Research Tooling Audit

> Working evidence register for the `subrojitroy10` GitHub profile. This is deliberately broader than a conventional software-engineering tech stack: it tracks scientific computing, computational physics, aerospace/detector modelling, AI/ML, product engineering, infrastructure and research methods.
>
> **Status:** research in progress. Do not copy every item into the public README yet.

## Evidence rules

- **A — directly verified:** present in a current repository/manfiest, public project description, or public technical artefact attributable to Subrojit.
- **B — user-confirmed historical work:** directly supplied by Subrojit in prior project history, but the original dissertation/notebook/source file has not yet been recovered in this audit.
- **C — unverified candidate:** plausible or commonly associated with the work, but not evidenced. **Do not add to the README.**

The final profile should distinguish **tools actually used** from **technical subjects studied**. General relativity, gravitational waves, orbital mechanics, MHD, etc. are domains/methods, not software badges.

---

## 1. Physics, Astrophysics & Computational Science

### Confirmed tools / computational methods

| Item | Evidence | What it was used for |
| --- | --- | --- |
| **Python** | A | Orthographic ray tracer for 3D radiative-transfer modelling; computational physics and numerical modelling. |
| **Object-oriented Python** | A | Ray/sphere intersection and radiative-transfer model structure. |
| **Ray tracing / volumetric path tracing** | A | Radiative transfer through a spherical gas-cloud model. |
| **Magnetohydrodynamics (MHD)** | A | Alfvén-wave modelling / plasma-physics simulation. |
| **MacCormack predictor–corrector scheme** | A | Numerical solution of the coupled PDE system used for Alfvén-wave simulation. |
| **von Neumann stability analysis** | A | Stability analysis of the MacCormack discretisation. |
| **Finite-difference / grid discretisation** | A | Spatial/temporal numerical treatment of the Alfvén-wave PDE system. |
| **Initial and boundary conditions** | A | Wave propagation/reflection modelling. |
| **Neumann boundary conditions** | A | Boundary treatment in the Alfvén-wave simulation. |
| **Signal extraction & parameter estimation** | A | Gravitational-wave data-analysis training/work during the Glasgow MSc. |
| **Line-profile analysis / model validation against theory** | A | Validation of radiative-transfer outputs while changing model parameters. |

### Confirmed scientific / engineering domains

These belong in a **Scientific Computing / Physics** part of the profile, but should not be presented as software products:

- **Astrophysical fluid dynamics** — A
- **Plasma physics / Alfvén waves** — A
- **Radiative transfer** — A
- **Gravitational-wave detection and data analysis** — A
- **General relativity** — A
- **Planetary-system dynamics** — A
- **Pulsars and supernovae** — A
- **Shock formation and particle acceleration** — A
- **Optical and radio astronomy instrumentation** — A
- **Rocket dynamics and transfer orbits** — A
- **Spacecraft protection / hazardous space environments** — A

### Public evidence currently recovered

- LinkedIn public profile: `https://in.linkedin.com/in/subrojitroy`
  - lists the **Modelling Alfvén Waves** project with MHD, numerical methods, domain discretisation, initial/boundary conditions and Neumann conditions;
  - lists **Radiative Transfer Modelling using Raytracing**, explicitly describing a Python orthographic ray tracer, volumetric path tracing, OOP ray/sphere intersections and line-profile analysis;
  - Glasgow education section records gravitational-wave signal extraction / parameter estimation, astrophysical fluid dynamics, instrumentation, rocket dynamics and transfer orbits.
- Physics Stack Exchange, user `subrojitroy`: `https://physics.stackexchange.com/questions/810020/solving-partial-differential-equations-using-maccormack-scheme-and-to-quantify-i`
  - directly records use of the **MacCormack scheme**, **von Neumann stability analysis**, coupled PDEs and **Alfvén-wave / MHD** simulation.

---

## 2. Aerospace / Detector & Engineering Modelling

| Item | Evidence | Notes |
| --- | --- | --- |
| **ANSYS** | B | Used in the MSc airborne antineutrino-detector concept developed for an AWACS-sized aircraft. |
| **CAD modelling** | B | Used for the airborne detector concept. **Exact CAD package still needs recovery.** |
| **Physics / mathematical detector modelling** | B | Core modelling layer of the airborne antineutrino detector concept. |
| **Airborne systems concept modelling** | B | Detector architecture constrained around an AWACS-sized aircraft concept. |

Historical project context already established: the antineutrino detector concept was expanded with **Andy Buckley** and presented at an international conference. The audit still needs the original dissertation/project material to recover the exact software/version/toolchain and detector/simulation stack.

---

## 3. AI, Machine Learning & Research Computing

### Directly verified in current Polynovea / research code

| Tool / library | Evidence | Current use signal |
| --- | --- | --- |
| **Python** | A | Behavioural/research pipelines, acquisition system backend and scientific computation. |
| **NumPy** | A | Numerical/research pipelines. |
| **SciPy** | A | Statistical moments and spatial-distance computation in behavioural/physics-inspired pipelines. |
| **scikit-learn** | A | StandardScaler, SGDClassifier/Regressor, Pipeline, model evaluation, KMeans, PCA. |
| **Hugging Face Transformers** (`@huggingface/transformers`) | A | Present in the Infrakinetic backend dependencies. |
| **OpenAI SDK / APIs** | A | Acquisition/research-system backend integration. |
| **Qdrant** | A | Vector/retrieval infrastructure in the Acquisition System backend. |
| **Redis** | A | Runtime/data infrastructure across current systems. |
| **PCA** | A | Behavioural/research calibration pipeline. |
| **K-Means clustering** | A | Behavioural/research calibration pipeline. |

### ML / modelling methods visible in the codebase

- supervised classification and regression — A
- standardisation / feature scaling — A
- train/test splitting and evaluation — A
- class weighting — A
- PCA — A
- K-Means clustering — A
- similarity / distance computation — A
- statistical distributional features (including skew/kurtosis) — A

---

## 4. Product & Platform Engineering — Polynovea Era

### Languages

- **Python** — A
- **TypeScript** — A
- **JavaScript** — A
- **SQL / PostgreSQL / PLpgSQL** — A
- **HTML / CSS** — A, but lower-value for the public profile than the system-level stack.
- **Bash / shell scripting** — A

### Frontend / product interfaces

- **React** — A
- **Next.js** — A
- **Vite** — A
- **Tailwind CSS** — A
- **Zustand** — A
- **React Flow / `@xyflow/react`** — A
- **Three.js / React Three Fiber / Drei** — A
- **GSAP** — A
- **Recharts** — A
- **BlockNote** — A

### Backend / APIs

- **Node.js** — A
- **Express** — A
- **FastAPI** — A
- **Uvicorn** — A
- **Pydantic** — A
- **REST / OpenAPI** — A
- **PostgreSQL drivers:** `pg`, `asyncpg` — A

### Data / storage / application infrastructure

- **PostgreSQL** — A
- **Redis / ioredis** — A
- **Supabase** — A
- **Qdrant** — A
- **S3 object storage** — A

### Documents / structured content

- **pdfme** — A
- **PDFKit** — A
- **Mammoth** — A
- **Marked / Markdown processing** — A
- **XLSX processing** — A

---

## 5. Cloud, Infrastructure & Operations

### AWS

Directly visible in current systems:

- **AWS S3** — A
- **AWS Lambda** — A
- **Amazon Cognito** — A
- **CloudWatch** — A
- **Event-driven AWS integrations / SDK** — A

### Azure

- **Azure Service Bus** — A
- **Azure-hosted container/service usage** — A

### Platform / deployment

- **Linux** — A
- **Nginx** — A
- **Git / GitHub** — A
- **GitHub Actions** — A
- **Vercel** — A
- **PM2** — A
- **Prometheus-compatible metrics (`prom-client`)** — A

---

## 6. Testing, Automation & Data Acquisition

- **Playwright** — A
- **Puppeteer** — A
- **Vitest** — A
- **Testing Library** — A
- browser rendering and lifecycle management — A
- deterministic structured-data extraction — A
- crawling / worker pools / checkpointing / rate limiting — A
- JSON-LD and hydration-state extraction — A
- LLM fallback extraction — A

---

## 7. Items specifically NOT yet verified

The following are **not** to be added to the GitHub README until evidence is recovered:

- MATLAB — C
- Mathematica / Wolfram — C
- Astropy — C
- Jupyter Notebook as a historical research tool — C
- pandas — C
- Matplotlib — C
- ROOT — C
- Geant4 — C
- CERN/HEP simulation packages — C
- Fortran — C
- C / C++ as a personal research language — C
- SolidWorks — C (CAD is confirmed; package is not)
- AutoCAD — C
- CATIA — C
- STK / Systems Tool Kit — C
- SPICE / NAIF — C
- OpenVSP — C

**Important:** Andy Buckley has worked with several particle-physics / HEP tools, but that is not evidence that Subrojit personally used those tools. They must not be inherited into this profile by association.

---

## 8. Proposed public-profile taxonomy

The eventual README should not use one undifferentiated badge wall. A more truthful structure is:

### Scientific Computing & Astrophysics
Python · Computational Physics · MHD · Numerical PDEs · MacCormack · Stability Analysis · Ray Tracing · Radiative Transfer · Gravitational-Wave Data Analysis

### Aerospace / Detector Modelling
ANSYS · CAD · Detector Modelling · Mathematical / Physics Simulation

### AI / ML & Research Computing
Python · NumPy · SciPy · scikit-learn · Hugging Face Transformers · PCA · Clustering · Qdrant · OpenAI

### Product & Platform Engineering
TypeScript · JavaScript · React · Next.js · Node.js · Express · FastAPI · PostgreSQL · Redis · Supabase

### Cloud & Infrastructure
AWS · Azure · Linux · Nginx · GitHub Actions · Vercel

### Testing / Automation / Acquisition
Playwright · Puppeteer · Vitest · Browser Automation · Crawling · Structured Extraction

This taxonomy tells the progression **physics → modelling → data/ML → enterprise systems**, instead of making the profile look like a generic full-stack badge collection.

---

## 9. Remaining recovery work

1. Recover the original **MSc project / dissertation / conference material** for the airborne antineutrino-detector concept.
2. Identify the exact **CAD package** used.
3. Recover old **Alfvén-wave and ray-tracing notebooks/code** if they still exist.
4. Search old CVs / coursework / project descriptions for exact Python scientific libraries and plotting/notebook tooling.
5. Recover any gravitational-wave coursework/project artefacts to distinguish methods learned from software actually used.
6. Check for orbital / aerospace simulation tooling rather than inferring it from subject knowledge.
7. Only after this audit is complete, redesign the README's `Selected Technical Stack` section and move the profile-views counter to a more obvious analytics location.
