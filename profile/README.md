# Tesserine

Autonomous AI agent runtime ecosystem. Tesserine provides the
infrastructure for running methodology-managed AI agents on your own
hardware — from container lifecycle to cognitive pipeline to the
methodology that teaches agents how to work.

## The Stack

| Component | Role |
|-----------|------|
| [**agentd**](https://github.com/tesserine/agentd) | Daemon that runs agent sessions in ephemeral Podman containers. Owns identity, credentials, scheduling, and lifecycle. |
| [**runa**](https://github.com/tesserine/runa) | Cognitive runtime inside the container. Loads a methodology, validates artifacts, enforces the dependency graph. |
| [**groundwork**](https://github.com/tesserine/groundwork) | Open-source contributor methodology. The first methodology plugin for runa. |
| [**base**](https://github.com/tesserine/base) | Reference container image. Wolfi-based, ships with the agentd contract and agent runtime tooling. |
| [**commons**](https://github.com/tesserine/commons) | Shared principles and design decisions across the ecosystem. |

## Architecture

The operator declares *what* — which agent, which methodology, which
project. The ecosystem owns *how* — container isolation, pipeline
enforcement, artifact validation. Each layer is independently useful and
independently replaceable: agentd manages the infrastructure, runa
enforces the cognitive pipeline, and methodology plugins define how
agents think and work. The agent gets an ephemeral workspace with exactly
what it needs and nothing more.

## Status

Pre-release. All components under active development toward v0.1.0.

## The Name

From *tessera* (mosaic tile — composition from modular pieces), *tesseract*
(higher-dimensional structure), and Madeleine L'Engle's verb *to tesser*
(folding through dimensions). The adjective form says this is about how
you do things. What you do is wide open.
