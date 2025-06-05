# Security Policy

## Supported Versions

The following versions of Auriora projects are currently being supported with security updates:

| Project | Supported Versions |
| ------- | ------------------ |
| Admin Assistant | latest |
| TimeLocker | latest |
| OneMount | latest |

## Reporting a Vulnerability

The Auriora team takes security vulnerabilities seriously. We appreciate your efforts to responsibly disclose your findings.

### How to Report a Vulnerability

If you believe you've found a security vulnerability in any Auriora project, please follow these steps:

1. **Do not disclose the vulnerability publicly** until it has been addressed by the maintainers.
2. Email your findings to [security@auriora.org](mailto:security@auriora.org). If you don't receive a response within 48 hours, please follow up.
3. Provide detailed information about the vulnerability, including:
   - **Project name** and version affected
   - **Description** of the vulnerability
   - **Steps to reproduce** the issue
   - **Potential impact** and severity assessment
   - **Affected components** (authentication, file handling, network communication, etc.)
   - **Suggestions** for mitigation or remediation

### What to Expect

After you report a vulnerability:

1. **Acknowledgment**: We will acknowledge receipt of your report within 48 hours.
2. **Investigation**: We will investigate the issue and determine its severity and impact.
3. **Communication**: We will keep you informed of our progress throughout the resolution process.
4. **Resolution**: Once the issue is resolved, we will coordinate the disclosure timeline with you.
5. **Recognition**: We will publicly acknowledge your responsible disclosure (unless you prefer to remain anonymous).

## Security Best Practices for Users

### Admin Assistant
- **Protect your Microsoft account**: Use strong passwords and enable two-factor authentication
- **Review permissions**: Only grant necessary OneDrive and calendar access
- **Keep updated**: Always use the latest version for security patches
- **Secure credentials**: Store authentication tokens securely
- **Monitor logs**: Review application logs for unusual activity

### TimeLocker
- **Backup encryption**: Always use strong passwords for backup repositories
- **Cloud credentials**: Secure your S3/B2 access keys and rotate them regularly
- **Local permissions**: Ensure backup files have appropriate filesystem permissions
- **Verify backups**: Regularly test backup integrity and restoration
- **Update dependencies**: Keep Restic and TimeLocker updated

### OneMount
- **Microsoft account security**: Use strong passwords and 2FA for your Microsoft account
- **Mount permissions**: Use appropriate mount point permissions
- **Network security**: Be cautious when using OneMount on untrusted networks
- **Cache security**: Understand that cached files are stored locally
- **Regular updates**: Keep OneMount updated for security patches

## Security Design Principles

Auriora projects follow these security principles:

### Authentication & Authorization
- **Minimal permissions**: Request only necessary permissions from external services
- **Secure authentication**: Use industry-standard OAuth 2.0 implementations
- **Token management**: Secure storage and handling of authentication tokens
- **Session management**: Proper session handling and timeout mechanisms

### Data Protection
- **Encryption in transit**: All network communications use HTTPS/TLS
- **Local encryption**: Sensitive data stored locally is properly protected
- **Data minimization**: Collect and store only necessary data
- **Secure deletion**: Proper cleanup of temporary and cached data

### Input Validation
- **Sanitization**: All user inputs are properly validated and sanitized
- **Path traversal protection**: Prevent directory traversal attacks
- **Command injection prevention**: Secure handling of system commands
- **File type validation**: Proper validation of file types and content

## Third-Party Dependencies

Our projects rely on various third-party libraries and services:

### Admin Assistant
- Microsoft Graph API
- Flask web framework
- SQLAlchemy ORM
- Various Python packages

### TimeLocker
- Restic backup tool
- Cloud storage SDKs (boto3, b2sdk)
- Python standard library

### OneMount
- Go standard library
- FUSE (go-fuse/v2)
- GTK3 (gotk3)
- Microsoft Graph API

We regularly review and update these dependencies to address known vulnerabilities.

## Vulnerability Disclosure Timeline

1. **Day 0**: Vulnerability reported
2. **Day 1-2**: Acknowledgment and initial assessment
3. **Day 3-7**: Detailed investigation and impact analysis
4. **Day 8-30**: Development and testing of fix
5. **Day 31-45**: Coordinated disclosure and patch release
6. **Day 46+**: Public disclosure (if not already disclosed)

This timeline may vary based on the complexity and severity of the vulnerability.

## Security Contacts

- **Primary**: [security@auriora.org](mailto:security@auriora.org)
- **Backup**: [conduct@auriora.org](mailto:conduct@auriora.org)
- **PGP Key**: Available upon request

## Acknowledgments

We would like to thank the following individuals who have helped improve the security of Auriora projects through responsible disclosure:

- [List will be updated as contributions are received]

## Legal

This security policy is provided in good faith. Auriora reserves the right to modify this policy at any time. Security researchers who follow this policy will not face legal action from Auriora for their research activities.
