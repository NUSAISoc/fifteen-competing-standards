# Contributing to FCS

## Development Setup
```bash
python -m pip install -U pip
python -m pip install -e ".[dev]"
```

## Design Layout
The codebase is organized into modules representing different AI/ML/DL standards. It is designed this way for maximum modularity and ease of extension.

In tree-structure:
```
src/fcs/
    |-- core/            # Universal interfaces and utilities
    |-- classical/       # Classical AI algorithms and data structures
    |-- ml/              # Machine Learning algorithms and models
    |-- dl/              # Deep Learning architectures, layers, etc.
    |
    |-- infra/           # Infrastructure code (datasets, logging, etc.)
    |-- cross_paradigm/  # Algorithms and utilities spanning multiple paradigms (such as RL, AI with ML heuristics, etc.)
    |-- end_to_end/      # Ready-made pipelines and workflows 
```

Any changes to the layout must be discussed and approved via issue or PR.

## Running Tests & Linters

We use `pytest` for testing.
```bash
pytest
```

Linting is done with `ruff`:
```bash
ruff check .
```

## Code Style & Formatting

1. Code must be cleanly written and well-documented, with the requisite type hints (incl. return types).
2. Try to follow [PEP 8](https://peps.python.org/pep-0008/).

For formatting matters, 
use `ruff`:
```bash
ruff format .
```