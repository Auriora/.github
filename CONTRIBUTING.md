# Contributing to Auriora Projects

Thank you for your interest in contributing to Auriora! This document provides guidelines and instructions for contributing to any project in our organization.

## Table of Contents

1. [Code of Conduct](#code-of-conduct)
2. [Getting Started](#getting-started)
3. [Development Environment](#development-environment)
4. [Project-Specific Guidelines](#project-specific-guidelines)
5. [Coding Standards](#coding-standards)
6. [Pull Request Process](#pull-request-process)
7. [Reporting Bugs](#reporting-bugs)
8. [Feature Requests](#feature-requests)

## Code of Conduct

This project and everyone participating in it is governed by the [Auriora Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. Please report unacceptable behavior to [conduct@auriora.org](mailto:conduct@auriora.org).

## Getting Started

1. **Choose a project**: Browse our [organization repositories](https://github.com/Auriora) to find a project that interests you
2. **Fork the repository** on GitHub
3. **Clone your fork** locally
4. **Add the original repository** as a remote named "upstream"
5. **Create a new branch** for your changes

```bash
git clone https://github.com/yourusername/project-name.git
cd project-name
git remote add upstream https://github.com/Auriora/project-name.git
git checkout -b feature/your-feature-name
```

## Development Environment

Each project has specific requirements. Please refer to the individual project's documentation:

### Admin Assistant (Python)
- Python 3.12+
- Virtual environment recommended
- Microsoft 365 account for testing
- See [Admin Assistant README](https://github.com/Auriora/admin-assistant/blob/main/README.md)

### TimeLocker (Python)
- Python 3.12+
- Restic backup tool
- Cloud storage accounts for testing (optional)
- See [TimeLocker README](https://github.com/Auriora/TimeLocker/blob/main/README.md)

### OneMount (Go)
- Go 1.23+
- GCC compiler
- webkit2gtk-4.0 and json-glib development headers
- Microsoft OneDrive account for testing
- See [OneMount README](https://github.com/Auriora/OneMount/blob/main/README.md)

## Project-Specific Guidelines

While this document provides general guidelines, each project may have additional specific requirements:

- **Admin Assistant**: Focus on Microsoft 365 integration, calendar management, and timesheet automation
- **TimeLocker**: Emphasize backup reliability, cross-platform compatibility, and user-friendly interfaces
- **OneMount**: Prioritize filesystem performance, FUSE integration, and seamless OneDrive access

Always check the project's individual `CONTRIBUTING.md` file for specific guidelines.

## Coding Standards

### General Principles

1. **Quality First**: Write clean, maintainable, and well-tested code
2. **Documentation**: Document public APIs and complex logic
3. **Testing**: Include comprehensive tests for new features
4. **Performance**: Consider performance implications of changes
5. **Security**: Follow security best practices for your language

### Language-Specific Standards

#### Python Projects (Admin Assistant, TimeLocker)
- Follow PEP 8 style guidelines
- Use type hints for function signatures
- Write docstrings for public functions and classes
- Use pytest for testing
- Maintain test coverage above 80%

#### Go Projects (OneMount)
- Follow Go's standard formatting (use `gofmt`)
- Write godoc-compatible comments
- Use Go's built-in testing framework
- Handle errors explicitly
- Use structured logging with zerolog

## Pull Request Process

1. **Ensure your code follows** the project's coding standards
2. **Update documentation** as necessary
3. **Add or update tests** as appropriate
4. **Ensure all tests pass** locally
5. **Update the changelog** if applicable
6. **Submit a pull request** with a clear description

### PR Requirements

- [ ] Code follows project coding standards
- [ ] Tests pass locally
- [ ] Documentation updated
- [ ] Changelog updated (if applicable)
- [ ] No merge conflicts
- [ ] Clear commit messages

## Reporting Bugs

When reporting bugs, please include:

1. **Clear and descriptive title**
2. **Steps to reproduce** the issue
3. **Expected behavior**
4. **Actual behavior**
5. **Environment information** (OS, language version, project version)
6. **Log output** or error messages
7. **Screenshots** if applicable

Use the appropriate issue template for your project.

## Feature Requests

Feature requests are welcome! Please provide:

1. **Clear and descriptive title**
2. **Detailed description** of the proposed feature
3. **Use cases** and benefits
4. **Implementation suggestions** (if any)
5. **Alternatives considered**

## Development Workflow

### Branching Strategy

- `main` - Stable, production-ready code
- `feature/description` - New features
- `bugfix/description` - Bug fixes
- `hotfix/description` - Critical fixes

### Commit Messages

Use clear, descriptive commit messages:

```
type(scope): brief description

Longer description if needed

Fixes #123
```

Types: `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`

## Community

- **GitHub Discussions**: For general questions and discussions
- **Issues**: For bug reports and feature requests
- **Pull Requests**: For code contributions
- **Email**: [contact@auriora.org](mailto:contact@auriora.org) for general inquiries

## Recognition

Contributors will be recognized in:
- Project README files
- Release notes
- GitHub contributor graphs
- Special recognition for significant contributions

Thank you for contributing to Auriora's mission of building better Linux utilities!
