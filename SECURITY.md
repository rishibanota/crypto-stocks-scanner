# Security Policy

## Reporting a Vulnerability

If you discover a security vulnerability in **Live Market Screener**, please report it responsibly.

- **Email:** rishibanota837@gmail.com
- Do not open a public issue for security vulnerabilities.
- Provide as much detail as possible, including steps to reproduce and potential impact.

We will acknowledge your report within **48 hours** and provide a detailed response within **7 days** outlining next steps and a timeline for a fix.

## Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| main    | :white_check_mark: |

## Security Considerations

- This project is a client-side only application (`index.html`) with no backend.
- WebSocket connections are made to the Delta Exchange public API.
- No secrets, API keys, or credentials are stored or transmitted by this application.
