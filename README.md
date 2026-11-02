# DevOps Projects

[![Code: AGPL-3.0](https://img.shields.io/badge/Code-AGPL--3.0-blue.svg)](LICENSE)
[![Content: CC BY-SA 4.0](https://img.shields.io/badge/Content-CC%20BY--SA%204.0-blue.svg)](LICENSE-CONTENT)
[![OpenSSF Scorecard](https://api.scorecard.dev/projects/github.com/vitorparras/DevOps-Projects/badge)](https://scorecard.dev/viewer/?uri=github.com/vitorparras/DevOps-Projects)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](CODE_OF_CONDUCT.md)
[![PRs welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

Practical DevOps references and projects: Docker, CI/CD pipelines, Kubernetes,
infrastructure as code and observability, in English and Brazilian Portuguese.

> **Status:** active. The Docker command guide is available; the other areas
> in the [roadmap](#roadmap) are planned.

## Table of contents

- [Available content](#available-content)
- [Roadmap](#roadmap)
- [Repository layout](#repository-layout)
- [Conventions](#conventions)
- [Contributing](#contributing)
- [Security](#security)
- [Code of conduct](#code-of-conduct)
- [License](#license)

## Available content

### Docker

A command guide with description, parameters and an example for each command,
from checking the installed version to building images, running containers,
inspecting logs and cleaning up.

| English | Português (BR) |
|---|---|
| [Docker Command Guide](<Docker/EN/Docker Command.md>) | [Guia de Comandos Docker](<Docker/BR/Comandos Docker.md>) |

## Roadmap

Planned areas, each with working configuration files and a README explaining
how to use and adapt them. Open a
[suggestion](https://github.com/vitorparras/DevOps-Projects/issues/new?template=content_suggestion.yml)
to propose another or to volunteer for one of these.

- **Docker**: multi-stage Dockerfiles, Compose for local environments, image
  hardening (non-root, minimal base, pinned digests).
- **CI/CD**: GitHub Actions pipelines with pinned actions, least-privilege
  permissions, caching, and release automation.
- **Kubernetes**: deployments, services, ingress, config and secrets, resource
  limits, health probes; Helm or Kustomize.
- **Infrastructure as code**: Terraform modules with remote state and policy
  checks.
- **Observability**: OpenTelemetry, Prometheus and Grafana dashboards.

## Repository layout

```text
DevOps-Projects/
├── Docker/
│   ├── EN/Docker Command.md
│   └── BR/Comandos Docker.md
├── .github/                 # Issue and PR templates, workflows, Dependabot
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── SECURITY.md
└── LICENSE
```

Each area has its own top-level folder. Documents exist in `EN/` and `BR/`
subfolders; configuration files are shared.

## Conventions

- **Everything runs.** Every configuration file is tested and states the tool
  version it was written for.
- **Secure by default**: least privilege, no secrets in files, pinned versions
  and digests, non-root containers.
- **Explain the why**, not only the how: each README says which problem the
  configuration solves and what the alternatives were.

## Contributing

New guides, configurations and corrections are welcome. Please read
[CONTRIBUTING.md](CONTRIBUTING.md) first. The `main` branch is protected and
only receives changes through reviewed pull requests.

## Security

Found a configuration that would lead a reader to an insecure setup, or a
problem in this repository? Follow [SECURITY.md](SECURITY.md) and report it
privately.

## Code of conduct

This project follows the [Contributor Covenant](CODE_OF_CONDUCT.md). By
participating you agree to uphold it.

## License

This repository uses two licenses:

- **Code** (programs, scripts, configuration files and code samples):
  [GNU Affero General Public License v3.0](LICENSE) (AGPL-3.0).
- **Content** (documents, explanations, images and other non-code material):
  [Creative Commons Attribution-ShareAlike 4.0 International](LICENSE-CONTENT)
  (CC BY-SA 4.0).

Both require attribution, and both require that modified versions you
distribute, sell or run as a network service remain under the same license.
Copyright © Vitor Hugo Parras.
