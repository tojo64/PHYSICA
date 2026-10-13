# PHYSICA — Autonomous Experimental Model Discovery

**From observing motion to discovering mathematical explanations and testing predictions.**

PHYSICA is a scientific computing project designed to investigate physical motion using data, mathematical models, uncertainty estimation, and experimental validation.

Its goal is to build a system that can observe an object moving through a physical experiment—such as a ball rolling down a ramp—extract measurements, compare competing mathematical models, identify the model best supported by the available evidence, predict unseen motion, and test those predictions against actual observations.

Rather than simply calculating answers from a predefined equation, PHYSICA aims to make the modelling and prediction process transparent, reproducible, and scientifically testable.

## What is PHYSICA intended to do?

- **Measure motion:** Obtain position and timing data from synthetic datasets and, as development progresses, real camera footage.
- **Discover supported models:** Fit and compare candidate mathematical equations instead of automatically assuming one explanation.
- **Estimate uncertainty:** Produce predictions with uncertainty intervals and communicate when reliable predictions cannot be made.
- **Predict unseen outcomes:** Estimate an object's position or crossing time at an unobserved point in its motion.
- **Validate predictions:** Compare predicted values with later observations and report errors and interval-based outcomes.
- **Preserve scientific integrity:** Distinguish measurements, calculations, model-supported conclusions, and predictions, while avoiding unsupported claims.

## Current implementation

The project has an established scientific software foundation, including:

- Scientific datasets and motion-trajectory processing.
- Candidate-model fitting and model selection.
- Prediction generation and bootstrap-based predictive intervals.
- Selection safeguards that refuse unreliable model outcomes.
- Deterministic prediction serialization and an offline prediction CLI.
- A validation comparison core with `MATCH`, `MISS`, and `INCONCLUSIVE` outcomes.
- Automated tests and documented acceptance criteria.

The Phase 9 validation work is in progress. Held-out observation leakage protection and validation-result serialization are being developed incrementally.

## Technology

PHYSICA is designed for CPU-based execution on modest hardware. Its scientific foundation uses Python, NumPy, SciPy, mathematical model evaluation, statistical methods, and automated testing. The intended camera-based system will use computer vision and a calibrated measurement pipeline.

The planned user interface is a professional scientific dashboard featuring motion tracking, trajectory charts, model comparisons, prediction intervals, validation results, and experiment history.

## Project dossier

The repository includes an interactive HTML project dossier that explains the project's purpose, architecture, scientific methods, technology choices, development roadmap, limitations, and planned science-fair demonstration.

## Development status

PHYSICA is under active development. The prediction pipeline has been implemented and checkpointed, while validation and the complete end-to-end experimental workflow remain in progress. The evidence-persistence integration and professional dashboard are planned work, not yet claimed as finished capabilities.

The long-term objective is to demonstrate a complete scientific loop:

**Observe → Measure → Model → Select → Predict → Validate → Learn**

The goal is not to claim that the software discovers universal laws of nature, but to identify which candidate models are best supported by its measurements and to test how well their predictions agree with reality.
