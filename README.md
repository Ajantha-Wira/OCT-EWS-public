# OCT Early Warning System (OCT-EWS)
A representation-space early warning system for detecting unsafe normal 
predictions in automated OCT screening using embedding-space geometry. 
This work forms the foundational framework for subsequent research on 
representation-space safety and distance-based modelling in medical AI.

> **Note:**
> This repository accompanies the research preprints and provides a 
> structured overview of the Early Warning System (EWS) framework. It 
> includes selected configuration details and documentation. The full 
> implementation, including source modules, notebooks, and test suite, 
> is maintained in a private repository and will be released in a future 
> public version at: github.com/Ajantha-Wira/OCT-EWS

## Overview
This repository presents the Early Warning System (EWS), a 
post-classification safety framework for detecting structurally atypical 
normal predictions in deep learning-based OCT screening. This work forms 
the foundational framework for subsequent research on representation-space 
safety and distance-based modelling in medical AI.

Unlike conventional uncertainty methods that rely on softmax confidence, 
the EWS operates in representation space, analysing embedding geometry to 
identify predictions that may be unsafe to accept automatically.

## Research Papers

**Paper 1 — EWS Framework**
> Wirasinghe, A. I. (2026)
> *An Embedding-Based Post-Classification Safety Layer for Detecting 
> Unsafe Normal Predictions in OCT Screening*
> https://doi.org/10.5281/zenodo.19748474

**Paper 2 — Distance Metric Analysis**
> Wirasinghe, A. I. (2026)
> *Distance Metrics for Representation-Space Safety: A Mahalanobis-Based 
> Analysis for Detecting Structurally Atypical Normal Predictions in 
> OCT Screening*
> https://doi.org/10.5281/zenodo.19775566

## Framework
The system consists of three sequential layers:
- **Layer A** — Mahalanobis distance-based atypicality detection
- **Layer B** — Disease-direction geometry analysis
- **Layer C** — Clinical prioritisation and workflow decisions

## Repository Structure
This public repository provides a conceptual and structural overview of 
the system architecture.

The full implementation includes modules for:
- data management and preprocessing
- reference distribution construction
- anomaly scoring (Mahalanobis distance)
- disease-direction analysis
- reporting and monitoring

The structure below outlines the full system architecture, including 
modules currently maintained in a private repository.

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
Details on leakage-corrected preprocessing are provided in the papers.

## Phase Design
- **Phase 1** — Empirical threshold-based detection (current implementation)
- **Phase 2** — Clinically validated thresholds (future work)

> Preliminary research output. Not intended for clinical decision-making.

## Citation
If you use this work, please cite the relevant paper(s):

**Paper 1:**
Wirasinghe, A.I. (2026) "An Embedding-Based Post-Classification Safety 
Layer for Detecting Unsafe Normal Predictions in OCT Screening". 
Zenodo. doi:10.5281/zenodo.19748474.

**Paper 2:**
Wirasinghe, A.I. (2026) "Distance Metrics for Representation-Space 
Safety: A Mahalanobis-Based Analysis for Detecting Structurally Atypical 
Normal Predictions in OCT Screening". 
Zenodo. doi:10.5281/zenodo.19775566.

## License
MIT License.

## Author
Wirasinghe, A. I. (2026)
MSc Computer Science with AI, Keele University
https://orcid.org/0009-0009-0785-0597
github.com/Ajantha-Wira

## Preprints and DOIs
Both papers are available as citable preprints with persistent DOIs 
via Zenodo. Versioned releases are maintained for reproducibility 
and timestamping.

Paper 1: https://doi.org/10.5281/zenodo.19748474
Paper 2: https://doi.org/10.5281/zenodo.19775566
