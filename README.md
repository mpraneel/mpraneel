<h1 align="center">Praneel Magapu</h1>

<p align="center">
  <em>Backend and systems software, with a focus on physical and embodied systems</em>
</p>

<p align="center">
  <a href="https://praneelmagapu.me"><img src="https://img.shields.io/badge/Portfolio-praneelmagapu.me-0A0A0A?style=flat-square&logo=safari&logoColor=white" alt="Portfolio"></a>
  <a href="https://linkedin.com/in/praneel-magapu"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:pmagapu@ncsu.edu"><img src="https://img.shields.io/badge/Email-pmagapu@ncsu.edu-CC0000?style=flat-square&logo=gmail&logoColor=white" alt="Email"></a>
  <img src="https://img.shields.io/badge/NC%20State-CS%20'27-CC0000?style=flat-square" alt="NC State">
</p>

---

I build backend and systems software, with a focus on physical and embodied systems:
robotics, perception, spatial reasoning.

The thread through my work is putting a hard, validated boundary between an unreliable
input and the rest of the system, whether that input is a sensor, a model, or a user.
Constraint enforcement at the edge, failure detection, and an explicit decision about
what happens when something is wrong.

<img src="https://img.shields.io/badge/C++17-00599C?style=flat-square&logo=cplusplus&logoColor=white"> <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white">
<img src="https://img.shields.io/badge/Eigen-1F425F?style=flat-square">
<img src="https://img.shields.io/badge/CMake-064F8C?style=flat-square&logo=cmake&logoColor=white">
<img src="https://img.shields.io/badge/Open3D-1E88E5?style=flat-square">
<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white">
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white">
<img src="https://img.shields.io/badge/Postgres-4169E1?style=flat-square&logo=postgresql&logoColor=white">

---

## Systems and Spatial

### [arm-kinematics](https://github.com/mpraneel/arm-kinematics)
`C++17` `Eigen` `SFML`

Planar manipulator library with a runtime supervisor. Forward kinematics, analytic and
damped least-squares IK, collision checking, manipulability visualization. A deliberately
unreliable scripted controller sits on top; the supervisor between them enforces joint
and velocity limits, checks reachability, guards against singular configurations, and
logs every rejection with a reason. Benchmarks constraint violations and intervention
rate with the supervisor on and off.

### kv-store
`C++17`

Durable key-value store with a write-ahead log. Append-only log, crash recovery on
startup, compaction, and a benchmark suite measuring write throughput against fsync
policy. Correctness verified by killing the process mid-write and replaying.

### [mesh-alignment-engine](https://github.com/mpraneel/mesh-alignment-engine)
`Python` `Open3D` `NumPy` `trimesh`

ICP-based 3D mesh registration. Nearest-neighbor correspondence, SVD-based rotation
estimation from the cross-covariance matrix, surface deviation heatmaps for visual
verification of alignment quality.

---

## Applied AI

### [hiring-agent](https://github.com/mpraneel/hiring-agent)
`FastAPI` `React` `Docker` `Pydantic`

Resume-to-JD matching pipeline. Pydantic contracts reject malformed LLM output at the API
boundary, hybrid keyword and semantic scoring produces a written rationale alongside each
score, ontology-based skill normalization maps equivalent skills to a common
representation. Dockerized with GitHub Actions CI.

### [mendacia](https://github.com/mpraneel/mendacia)
`React` `TypeScript` `Flask` `TwelveLabs`

Multimodal video forensics platform, HackNCState 2026. TwelveLabs scene segmentation and
transcript extraction, LLM narrative claim extraction, rule-based cross-modal comparison
flagging mismatches between what a video says and what it shows. An adapter layer
normalizes every backend response into a strict UI schema, isolating application state
from model output variance.

---

## Background

| Where | What |
|---|---|
| **Align Technology** <br> SWE Intern, R&D | 3D computational geometry and mesh processing in C++ and Python. Implemented ICP from scratch against a production scientific computing stack. |
| **DevDynamics.ai** <br> SWE Intern | Gmail workflow intelligence backend. Deterministic classifier on the fast path with an LLM fallback on low-confidence cases, both mapped into one fixed label schema. Per-thread stateful tracking, Supabase persistence, deployed on AWS. |
| **NC State, Game2Learn Lab** <br> Research Assistant | MerryQuery, a production RAG system deployed in a live classroom pilot. |
| **NC State, Dr. Gehringer** <br> Research Assistant | Crowd label quality control. Interval analysis and iterative aggregation to detect unreliable annotations at scale. |
| **Liquid Rocketry Lab** <br> Data Engineer | Real-time telemetry pipeline with containerized microservices and sub-second abort event capture. |

---

## Foundations

**Languages:** C++17, Python, Java, C
**Math and theory:** Linear algebra, numerical optimization, probability and statistics
**Systems:** Data structures, memory model, systems programming, storage and durability
**Focus:** Kinematics and motion planning, state estimation, runtime monitoring and
constraint enforcement
