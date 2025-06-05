# Support for Auriora Projects

This document outlines how to get help with any Auriora project. Please read through the available support options below.

## Table of Contents

1. [Project-Specific Documentation](#project-specific-documentation)
2. [General Troubleshooting](#general-troubleshooting)
3. [Community Support](#community-support)
4. [Reporting Issues](#reporting-issues)
5. [Feature Requests](#feature-requests)
6. [Security Issues](#security-issues)
7. [Commercial Support](#commercial-support)

## Project-Specific Documentation

Before seeking support, please check the documentation for your specific project:

### Admin Assistant
- [README](https://github.com/Auriora/admin-assistant/blob/main/README.md) - Overview and basic usage
- [Getting Started Guide](https://github.com/Auriora/admin-assistant/blob/main/docs/user-guides/UG-001-Getting-Started.md)
- [CLI Reference](https://github.com/Auriora/admin-assistant/blob/main/docs/user-guides/UG-002-CLI-Reference.md)
- [Troubleshooting Guide](https://github.com/Auriora/admin-assistant/blob/main/docs/user-guides/UG-003-Troubleshooting.md)

### TimeLocker
- [README](https://github.com/Auriora/TimeLocker/blob/main/README.md) - Project overview and features
- [Installation Guide](https://github.com/Auriora/TimeLocker/blob/main/docs/INSTALLATION.md)
- [Command Builder Documentation](https://github.com/Auriora/TimeLocker/blob/main/docs/command_builder.md)

### OneMount
- [README](https://github.com/Auriora/OneMount/blob/main/README.md) - Overview and basic usage
- [Quickstart Guide](https://github.com/Auriora/OneMount/blob/main/docs/guides/quickstart-guide.md)
- [Installation Guide](https://github.com/Auriora/OneMount/blob/main/docs/guides/installation-guide.md)
- [Troubleshooting Guide](https://github.com/Auriora/OneMount/blob/main/docs/guides/troubleshooting-guide.md)

## General Troubleshooting

### Common First Steps

1. **Check the project version**: Ensure you're using the latest version
2. **Review the logs**: Most projects provide detailed logging
3. **Check system requirements**: Verify your system meets the project requirements
4. **Restart the application**: Sometimes a simple restart resolves issues

### Admin Assistant Troubleshooting

```bash
# Check service status
systemctl --user status admin-assistant

# View logs
journalctl --user -u admin-assistant --since today

# Test Microsoft Graph connection
admin-assistant login msgraph --user <USER_ID>

# Validate configuration
admin-assistant config validate --user <USER_ID>
```

### TimeLocker Troubleshooting

```bash
# Test basic functionality
timelocker --version

# Check Restic installation
restic version

# Test repository access
timelocker list --repository /path/to/repo --password mypassword

# Enable debug logging
TIMELOCKER_DEBUG=1 timelocker backup --repository /path/to/repo
```

### OneMount Troubleshooting

```bash
# Check service status
systemctl --user status onemount@.service

# View logs
journalctl --user -u onemount@.service --since today

# Enable debug mode
ONEMOUNT_DEBUG=1 onemount /mount/path

# Unmount and remount
fusermount3 -uz /mount/path
onemount /mount/path
```

## Community Support

Get help from the community and project maintainers:

### GitHub Resources
- **Issues**: Browse existing issues to see if your problem has been reported
  - [Admin Assistant Issues](https://github.com/Auriora/admin-assistant/issues)
  - [TimeLocker Issues](https://github.com/Auriora/TimeLocker/issues)
  - [OneMount Issues](https://github.com/Auriora/OneMount/issues)

- **Discussions**: For general questions and community discussions
  - [Organization Discussions](https://github.com/orgs/Auriora/discussions)

### Communication Channels
- **Email**: [support@auriora.org](mailto:support@auriora.org) for general support
- **GitHub**: Primary platform for technical discussions and issue tracking

## Reporting Issues

### Bug Reports

When reporting bugs, please include:

1. **Project name and version**
2. **Operating system and version**
3. **Clear description** of the issue
4. **Steps to reproduce** the problem
5. **Expected vs. actual behavior**
6. **Log output** or error messages
7. **Screenshots** if applicable
8. **Configuration details** (sanitized of sensitive information)

### Information to Gather

#### Admin Assistant
- Python version
- Virtual environment details
- Microsoft 365 account type
- CLI command used
- Database schema version

#### TimeLocker
- Python version
- Restic version
- Storage backend type (Local/S3/B2)
- Backup repository details
- File selection patterns

#### OneMount
- Go version
- Linux distribution and version
- FUSE version
- OneDrive account type
- Mount point and permissions

## Feature Requests

We welcome suggestions for new features:

1. **Check existing requests**: Search issues for similar feature requests
2. **Provide detailed description**: Explain the feature and its benefits
3. **Include use cases**: Describe specific scenarios where this would be helpful
4. **Consider implementation**: If possible, suggest how it might be implemented

## Security Issues

For security-related issues, please refer to our [Security Policy](SECURITY.md) and follow the vulnerability reporting process outlined there.

**Do not report security issues through public GitHub issues.**

## Commercial Support

While Auriora projects are open source and community-supported, commercial support options may be available:

- **Consulting**: Custom implementation and integration services
- **Training**: Team training on project usage and best practices
- **Priority Support**: Expedited issue resolution and feature development
- **Custom Development**: Tailored features for specific organizational needs

Contact [business@auriora.org](mailto:business@auriora.org) for commercial support inquiries.

## Support Timeline

Auriora projects are maintained by volunteers and contributors. Response times may vary based on:

- **Issue severity**: Security issues and critical bugs receive priority
- **Complexity**: Simple issues may be resolved quickly, complex ones take longer
- **Maintainer availability**: Response times depend on volunteer availability
- **Community involvement**: Active community participation helps everyone

### Priority Levels

1. **Critical**: Security vulnerabilities, data loss issues
2. **High**: Major functionality broken, blocking workflows
3. **Medium**: Minor bugs, performance issues
4. **Low**: Feature requests, documentation improvements

## Getting Involved

The best way to get support is to become part of the community:

- **Contribute**: Help fix bugs and implement features
- **Document**: Improve documentation and guides
- **Test**: Help test new releases and report issues
- **Support Others**: Answer questions and help other users

Thank you for using Auriora projects!
