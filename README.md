# 3DMicroStructLab

[![License: Apache 2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)

3DMicroStructLab is an open-source Python toolkit for reconstructing and studying
three-dimensional fibrous microstructures. It is being extracted from a private
research codebase into a reproducible, testable package for scientific use and
collaboration.

> **Project status:** pre-alpha scaffold. The scientific implementation and its
> validated examples will be migrated incrementally. The current `0.0.0` package
> establishes the public project structure but does not yet expose the research
> pipeline.

## Intended workflow

The project will provide one package, `microstructlab`, for three main stages:

1. **Processing:** derive fiber coordinates, orientations, and slice statistics
   from CT-scan data.
2. **Modelling and generation:** fit latent statistical models and generate
   synthetic microstructures with packing and overlap constraints.
3. **Validation and export:** compare synthetic and measured structures and
   export geometry for downstream analysis.

Core logic belongs under `src/microstructlab/`. Notebooks will remain thin,
configuration-driven demonstrations, while cluster scripts and publication
artifacts stay separate from the reusable library.

## Installation

The project currently requires Python 3.10 or newer. For development, clone the
repository and install it in editable mode:

```bash
python -m venv .venv
python -m pip install --upgrade pip
python -m pip install -e ".[dev]"
```

A Conda environment and pinned scientific dependencies will be added as the
corresponding modules are migrated and verified.

## Quickstart

The scaffold can be imported and queried for its version:

```python
import microstructlab

print(microstructlab.__version__)
```

Runnable scientific examples will be added under `examples/` using small,
shareable synthetic datasets. Large or restricted CT data and generated results
will not be committed to this repository.

## Repository layout

- `src/microstructlab/`: reusable Python package and single source of truth
- `tests/`: fast tests built around deterministic synthetic fixtures
- `configs/`: versioned model and pipeline configuration
- `notebooks/`: numbered, thin research workflows
- `scripts/`: local batch and conversion utilities
- `scripts-hpc/`: cluster-specific submission infrastructure
- `examples/`: self-contained demonstrations with tiny data
- `docs/`: theory, API, and pipeline documentation
- `data/`: provenance and access instructions, not research data
- `results/`: ignored generated outputs
- `paper/`: publication-specific reproduction material

## Citation

Citation metadata will be added in `CITATION.cff` once the publication authors,
title, and DOI or archival identifier are finalized. Until then, please cite the
repository URL and the version or commit used.

## Contributing

The public contribution workflow and code of conduct will be added before the
first development release. Please use an issue to discuss substantial changes
before opening a pull request.

## License

Copyright 2026 Mohamad A. Raja.

This project is licensed under the [Apache License 2.0](LICENSE). Confirm any
institutional ownership, third-party code, and data-sharing obligations with TU
Delft before publishing migrated private-project material.
