# Contributing to GoChat Server

Thank you for considering contributing to GoChat Server! We are excited to collaborate with you to enhance this project. GoChat provides a secure messaging system using Go, and we value contributions from the community to make it even better. Here are the guidelines to help you contribute effectively.

## Table of Contents
- [Getting Started](#getting-started)
- [How to Contribute](#how-to-contribute)
  - [Reporting Issues](#reporting-issues)
  - [Feature Requests](#feature-requests)
  - [Pull Requests](#pull-requests)
- [Development Setup](#development-setup)
- [Code Style Guidelines](#code-style-guidelines)
- [Commit Messages](#commit-messages)
- [Code of Conduct](#code-of-conduct)

## Getting Started

If you're new to open source contributions, we recommend checking out [First Contributions](https://github.com/firstcontributions/first-contributions) to get an overview of how to contribute to GitHub projects.

To contribute to GoChat Server, follow these steps:

1. **Fork the Repository**: Visit [GoChat Server GitHub Repo](https://github.com/GoChatOrg/gcserver) and click the "Fork" button to create your copy of the repository.
2. **Clone the Forked Repository**: Clone your fork to work on it locally.
   ```bash
   git clone https://github.com/YOUR_USERNAME/gcserver.git
   ```
3. **Create a Branch**: Create a feature branch to isolate your work.
   ```bash
   git checkout -b feature/your-feature-name
   ```
4. **Make Changes**: Implement your changes or improvements.
5. **Run Tests**: Ensure all existing and new tests pass.
6. **Commit Your Changes**: Follow our [commit message guidelines](#commit-messages).
7. **Push Your Branch**: Push to your forked repository.
   ```bash
   git push origin feature/your-feature-name
   ```
8. **Submit a Pull Request (PR)**: Go to the [GoChat Server GitHub repository](https://github.com/GoChatOrg/gcserver) and open a PR from your branch.

## How to Contribute

### Reporting Issues

If you discover bugs or have questions, please open an issue. You can do so by following these steps:

- Navigate to the [Issues tab](https://github.com/GoChatOrg/gcserver/issues).
- Click on "New Issue."
- Provide a clear and descriptive title, and fill in the details of the problem.
- If you can, include steps to reproduce the issue, expected behavior, and relevant information such as environment details.

### Feature Requests

We welcome suggestions for new features! To propose a feature:

- Open a new issue and label it with `enhancement`.
- Describe the feature, use cases, and any relevant details on why it would improve the project.
- Feel free to discuss your idea with us before starting development.

### Pull Requests

- Make sure there is an issue that explains the context of your PR before creating a pull request.
- Clearly describe the purpose of your PR. Reference the issue number it addresses (e.g., `Fixes #123`).
- Ensure your changes do not break existing functionality.
- Before submitting, verify your code by running all tests and lint checks.

## Development Setup

To start contributing to GoChat Server, follow these steps:

### Prerequisites
- **Go 1.24+**: Ensure you have Go installed. [Download Go](https://golang.org/dl/).
- **Git**: Git is required to clone and create branches.

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/GoChatOrg/gcserver.git
   cd gcserver
   ```
2. Install dependencies:
   ```bash
   go mod tidy
   ```

## Code Style Guidelines

- Follow idiomatic Go conventions. For reference, see [Effective Go](https://go.dev/doc/effective_go).
- Run `go fmt` before committing your code.
- Code should be thoroughly documented, especially exported functions and types.
- All new functionality should have associated unit tests. Aim for high code coverage.

## Commit Messages

- Write meaningful commit messages. Use the present tense and keep messages concise.
- Example commit messages:
  - `Add feature X to improve performance`
  - `Fix bug in message encryption flow`
  - `Update README with setup instructions`

## Code of Conduct

This project adheres to the Contributor Covenant [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. Please report unacceptable behavior to the repository maintainers.

---

Thank you for contributing to GoChat Server! We value your time, ideas, and efforts and look forward to seeing your contributions.

For any questions, feel free to ask in the [discussions](https://github.com/GoChatOrg/gcserver/discussions) tab or by tagging maintainers in an issue.
