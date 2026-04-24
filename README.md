# OCT Early Warning System (OCT-EWS)

A representation-space early warning system for detecting unsafe normal predictions in automated OCT screening using embedding-space geometry. This work forms the foundational framework for subsequent research on representation-space safety and distance-based modelling in medical AI.


> **Note:**
> This repository accompanies the research preprint and
> provides a structured overview of the Early Warning System (EWS)
> framework. It includes selected configuration details and documentation.
> The full implementation, including source modules, notebooks,
> and test suite, is maintained in a private repository and will be
> released in a future public version at: github.com/Ajantha-Wira/OCT-EWS


## Overview

This repository presents the Early Warning System (EWS), a post-classification safety framework for detecting structurally atypical normal predictions in deep learning-based OCT screening. This work forms the foundational framework for subsequent research on representation-space safety and distance-based modelling in medical AI.

The work is introduced in:

> Wirasinghe, A. I. (2026)  
> *An Embedding-Based Post-Classification Safety Layer for Detecting Unsafe Normal Predictions in OCT Screening*  
> [Zenodo DOI – to be updated]

Unlike conventional uncertainty methods that rely on softmax confidence, the EWS operates in representation space, analysing embedding geometry to identify predictions that may be unsafe to accept automatically.

## Framework

The system consists of three sequential layers:

- **Layer A** — Mahalanobis distance-based atypicality detection
- **Layer B** — Disease-direction geometry analysis
- **Layer C** — Clinical prioritisation and workflow decisions

## Repository Structure

This public repository provides a conceptual and structural overview of the system architecture.

The full implementation includes modules for:
- data management and preprocessing
- reference distribution construction
- anomaly scoring (Mahalanobis distance)
- disease-direction analysis
- reporting and monitoring

The structure below reflects the full implementation architecture (private repository).
```
OCT_EWS/
├── config/          # Phase configuration and defaults
├── src/             # Core modules
│   ├── data_manager.py
│   ├── reference_builder.py
│   ├── anomaly_scorer.py
│   ├── direction_analyzer.py
│   ├── ews_scorer.py
│   ├── patient_monitor.py
│   └── report_generator.py
├── notebooks/       # Demonstration and analysis notebooks
├── tests/           # Test suite
└── main.py
```
The structure below reflects the full implementation architecture (private repository).

## Requirements

- Python 3.10
- PyTorch
- scikit-learn
- numpy
- pandas
- matplotlib

## Dataset

Experiments are based on the Kermany OCT2017 dataset.

Due to licensing restrictions, raw data is not included.  
Details on leakage-corrected preprocessing are provided in the paper.

## Phase Design

- **Phase 1** — Empirical threshold-based detection (current implementation)  
- **Phase 2** — Clinically validated thresholds (future work)

> Preliminary research output. Not intended for clinical decision-making.


## Citation

If you use this work, please cite:

Wirasinghe, A. I. (2026)
*An Embedding-Based Post-Classification Safety Layer for Detecting Unsafe Normal Predictions in OCT Screening*
[Zenodo DOI]

## License

MIT License.

## Author

Wirasinghe, A. I. (2026)
MSc Computer Science with AI, Keele University  
github.com/Ajantha-Wira

## Preprint and DOI

This work is available as a citable preprint with a persistent DOI:

[Zenodo DOI – to be updated]

A versioned release is maintained via Zenodo for reproducibility and timestamping.
