# Auriora Organization Configuration

This repository contains the public organization-wide configuration and community health files for the Auriora GitHub organization.

## Repository Purpose

The `.github` repository serves as the **public configuration hub** for the Auriora organization, providing:

- **Community Health Files**: Code of conduct, contributing guidelines, security policy, and support information
- **Issue & PR Templates**: Standardized templates for bug reports, feature requests, and pull requests
- **Workflow Templates**: Reusable GitHub Actions workflows for CI/CD processes
- **Organization Profile**: Public-facing information about Auriora and our projects

## How It Works

### File Inheritance
GitHub automatically discovers and inherits files from this repository across all Auriora projects:

1. **Community Health Files** (CODE_OF_CONDUCT.md, CONTRIBUTING.md, etc.) are inherited by repositories that don't have their own versions
2. **Issue and PR Templates** appear in all organization repositories
3. **Workflow Templates** are available in the Actions tab when creating new workflows
4. **Organization Profile** (profile/README.md) appears on the Auriora organization page

### Repository Structure

```
.github/
├── CODE_OF_CONDUCT.md              # Organization-wide code of conduct
├── CONTRIBUTING.md                 # General contributing guidelines
├── SECURITY.md                     # Security policy and vulnerability reporting
├── SUPPORT.md                      # Support resources and contact information
├── FUNDING.yml                     # GitHub sponsorship configuration
├── profile/
│   └── README.md                   # Organization profile page
└── .github/
    ├── ISSUE_TEMPLATE/             # Issue templates for all repos
    │   ├── bug_report.md
    │   ├── feature_request.md
    │   └── config.yml
    ├── PULL_REQUEST_TEMPLATE.md    # PR template for all repos
    ├── DISCUSSION_TEMPLATE/        # Discussion templates
    │   └── general.yml
    └── workflow-templates/         # Reusable GitHub Actions workflows
        ├── python-ci.yml
        ├── go-ci.yml
        ├── release.yml
        └── *.properties.json
```

## Auriora Projects

This configuration supports our Linux utility projects:

- **[Admin Assistant](https://github.com/Auriora/admin-assistant)** - Calendar management and timesheet automation for Microsoft 365
- **[TimeLocker](https://github.com/Auriora/TimeLocker)** - High-level backup interface using Restic
- **[OneMount](https://github.com/Auriora/OneMount)** - Mount Microsoft OneDrive as a native Linux filesystem

## Usage for Contributors

### For External Contributors
- All templates and guidelines in this repository apply to contributions across Auriora projects
- Use the issue templates when reporting bugs or requesting features
- Follow the contributing guidelines and code of conduct
- Reference the security policy for vulnerability reporting

### For Maintainers
- Update organization-wide policies by modifying files in this repository
- Add new workflow templates to share CI/CD patterns across projects
- Customize issue templates to improve bug reporting and feature requests
- Maintain consistent branding and documentation standards

## Related Repository

- **[.github-private](https://github.com/Auriora/.github-private)** - Private organizational configuration for internal processes and sensitive workflows


---

*Building better Linux utilities through collaborative development.*