# Sample Rust HTTP Service (Application & CI)

This repository houses the core application logic and Continuous Integration (CI) engine for a microservice architecture. By decoupling application code from deployment configurations, this repository simulates an enterprise-grade developer workflow.

### Key Features & CI/CD Architecture
* **High-Performance Backend:** A lightweight, containerized HTTP application written in Rust.
* **Automated CI Pipeline:** GitHub Actions workflow triggered on every `push` or `PR` to `main`.
* **Secure Containerization:** Builds and pushes minimal, multi-stage Docker images to [GitHub Container Registry (GHCR) / Docker Hub].
* **Automated Promotion:** The final CI step dispatches a repository dispatch event to the `promote_pipeline` repository, passing the new image tag to automate the GitOps delivery chain.
