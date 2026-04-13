# Tesserine

Self-hosted agent runtime. Tesserine runs autonomous AI agents on your
own hardware — managing container lifecycle, enforcing cognitive
methodology, and giving each agent an ephemeral workspace with exactly
what it needs and nothing more.

## The Stack

| Component | Role |
|-----------|------|
| [**agentd**](https://github.com/tesserine/agentd) | Daemon that runs agent sessions in ephemeral Podman containers. Owns identity, credentials, scheduling, and lifecycle. |
| [**runa**](https://github.com/tesserine/runa) | Cognitive runtime inside the container. Loads a methodology, validates artifacts, enforces the dependency graph. |
| [**groundwork**](https://github.com/tesserine/groundwork) | Open-source contributor methodology. The first methodology plugin for runa. |
| [**base**](https://github.com/tesserine/base) | Reference container image. Wolfi-based, ships with the agentd contract and agent runtime tooling. |
| [**commons**](https://github.com/tesserine/commons) | Shared principles and design decisions across the ecosystem. |

## Architecture

Tesserine is a strongly typed cognitive state machine. Methodologies
declare the topology — what artifacts exist, what protocols produce them,
what conditions must hold before and after each transition. The runtime
enforces fidelity: artifacts are validated against schemas, protocols
fire only when their dependencies are satisfied, and the agent receives
its work through typed interfaces that accept only well-formed output.
The value comes from the guarantee that any declared cognitive process
executes faithfully, regardless of its shape.

The operator declares *what* — which agent, which methodology, which
project. The runtime owns *how* — container isolation, pipeline
enforcement, artifact validation. Each layer is independently useful and
independently replaceable: agentd manages the infrastructure, runa
enforces the cognitive pipeline, and methodology plugins define how
agents think and work.

## Status

v0.1.0 released. All ecosystem components tagged and under active testing.

## The Name

From *tessera* (mosaic tile — composition from modular pieces), *tesseract*
(higher-dimensional structure), and Madeleine L'Engle's verb *to tesser*
(folding through dimensions). The adjective form says this is about how
you do things. What you do is wide open.
