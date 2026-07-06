# TensorBoard: Software Architecture Project

Software engineering coursework project analyzing the architecture of
[TensorBoard](https://github.com/tensorflow/tensorboard), the visualization
toolkit for TensorFlow / PyTorch / JAX training runs.

I reverse-engineered every class diagram and system dynamics diagram in
this repository directly from the TensorBoard source code, not from the
World & Machine Model. I checked each class name, method signature, and
field visibility against the actual repository. Each diagram's
description below cites the source files it draws from.

## Contents

| Section | Description |
|---|---|
| [World & Machine Model](docs/world-machine-model.md) | External assumptions, requirements, specifications |
| [Logical & Physical Architecture](docs/architecture.md) | High-level system structure and deployment |
| [Class Diagrams](docs/class-diagrams.md) | Static structure, grounded in real TensorBoard source |
| [System Dynamics Diagrams](docs/system-dynamics.md) | Sequence, state, and activity diagrams |

## Source

The diagrams come from the public repository:
[github.com/tensorflow/tensorboard](https://github.com/tensorflow/tensorboard)

Key files referenced throughout this project:
- `tensorboard/program.py`: server bootstrap
- `tensorboard/backend/application.py`: WSGI app / request routing
- `tensorboard/plugins/base_plugin.py`: plugin framework
- `tensorboard/default.py`: plugin registry (static + dynamic)
- `tensorboard/backend/event_processing/*`: event ingestion pipeline
- `tensorboard/data/provider.py`: data provider domain model
- `tensorboard/notebook.py`: Jupyter/Colab integration
