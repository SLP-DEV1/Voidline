# Security Policy

## Supported versions

The repository currently publishes one active release line. Security and compatibility reports should target the latest tagged release unless the problem also affects the current `main` branch.

## What counts as a security issue

Useful reports include issues such as:

- Exposed credentials, tokens, or private data
- Unsafe file handling or arbitrary file writes
- Unexpected code execution outside the application's intended behavior
- Dependency vulnerabilities with a realistic impact on this project
- Insecure update, download, or configuration behavior

Anti-cheat detection, ban avoidance, or requests to make the software harder to detect are **not** treated as security vulnerabilities.

## Reporting

If GitHub private vulnerability reporting is available for this repository, prefer that for sensitive reports. Otherwise, avoid posting secrets, personal data, or weaponized exploit details in a public issue.

A useful report should include:

- Affected release/tag
- Windows and .NET versions
- Reproduction steps
- Security impact
- Minimal proof of concept when needed to demonstrate the issue
- Any suggested mitigation

## Disclosure

Please give maintainers a reasonable opportunity to investigate a legitimate security issue before publishing sensitive technical details.
