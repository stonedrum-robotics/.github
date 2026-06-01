# Contributing

Thanks for helping improve the dexterous hands platform.

## Ways to contribute

- Report bugs with hardware setup, drivers, or examples.
- Suggest new grasp primitives or demo scenarios.
- Improve documentation and tutorials.
- Add support for additional hand models through the hardware abstraction layer.

## Development workflow

1. Open an issue describing the change.
2. Fork the repository and create a focused branch.
3. Run linting, type checks, and tests locally.
4. Open a pull request with a concise description and test notes.

## Coding standards

- Python code uses type hints and docstrings for public classes and functions.
- Hardware-facing logic must fail safely and document assumptions.
- Examples should run without physical hardware whenever a simulation or mock mode is available.
- Public APIs should remain vendor-neutral unless a vendor-specific adapter is unavoidable.

## Local checks

```bash
ruff check .
mypy dexterous_hand
pytest
```
