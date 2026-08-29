# Security Policy

Aserno ApS takes security seriously and values responsible disclosure. This policy explains how to report suspected security vulnerabilities affecting Aserno-maintained software, services, and repositories, how reports are triaged, and how coordinated disclosure is handled.

## Scope and Applicability

This is Aserno ApS' organization-wide default security policy. It applies to repositories maintained by Aserno ApS that do not provide their own `SECURITY.md`. A repository-specific security policy takes precedence when present.

This policy may apply to both public and proprietary projects.

Security reports are appropriate for vulnerabilities affecting:

- Aserno-maintained source code, applications, packages, and developer tools
- Official release artifacts and distribution mechanisms maintained by Aserno
- Authentication, authorization, request handling, configuration, persistence, APIs, CLI tools, or other application components
- Aserno-operated services where a vulnerability could affect confidentiality, integrity, or availability
- Supply-chain paths that could compromise Aserno software, services, or their users

Third-party software and services are outside the scope of this policy unless the reported vulnerability results directly from Aserno's integration, configuration, or use of them.

## Supported Versions

Security fixes target actively maintained release lines, branches, applications, and services.

When a repository or product documents supported versions, that repository- or product-specific information is authoritative.

As a default:

- The current maintained release line, branch, or deployed version receives priority
- Older maintained versions may receive fixes when severity, exploitability, customer impact, and backport risk justify it
- End-of-life or otherwise unsupported versions may require upgrading to a maintained version
- Proprietary applications and services are remediated according to their current supported deployment and maintenance status

Exact product inventories and version support can change over time, so repository- or product-specific information should be used when available.

## Reporting a Vulnerability

Please do **not** open a public issue, discussion, pull request, or other public report for a suspected security vulnerability before coordinated disclosure.

Preferred reporting channels:

- Email: **security@aserno.com**
- If the affected repository offers GitHub's **Report a vulnerability** action under Security Advisories, you may use that private reporting channel instead

Include, as applicable:

- The affected repository, product, application, service, or package
- The affected version, release, commit, or deployment where known
- A clear description of the vulnerability and its potential impact
- Minimal, deterministic reproduction steps or proof of concept
- Relevant environment details, such as runtime version, operating system, web server, browser, database, or deployment mode
- Relevant configuration details with secrets removed
- Sanitized logs, stack traces, screenshots, request/response examples, or other supporting evidence
- Any known mitigations or conditions required for exploitation

For exposed secrets, credentials, API keys, or tokens, revoke or rotate them first where possible.

Do not send active secrets unless they are essential to the report and a secure transfer method has been agreed in advance.

## Triage and Communication

We aim to:

- **Acknowledge** a report within **72 hours**
- Provide an **initial assessment** within **7 days**
- Communicate meaningful status changes while a valid issue is being investigated and remediated

These are response goals, not guarantees. Complex issues, incomplete reports, dependencies on third parties, or coordination with customers and downstream users may require additional time.

During triage, a report may be classified as valid, not reproducible, duplicate, out of scope, or requiring additional information.

## Severity and Remediation

We use **CVSS v4.0** where practical and may also provide a **CVSS v3.1** score when required for ecosystem or tooling compatibility.

CVSS is one input to prioritization.

We also consider:

- Real-world exploitability
- Affected users, customers, applications, and services
- Default exposure
- Confidentiality, integrity, and availability impact
- Data sensitivity
- Available mitigations
- Supply-chain implications
- Operational and downstream impact

For valid vulnerabilities, remediation priority is based on risk.

Where feasible, temporary configuration, operational, or deployment mitigations may be provided before a permanent fix is available.

## Fix and Disclosure Process

1. Reproduce the issue and determine root cause and affected scope.
2. Identify affected and supported versions, deployments, branches, products, or services.
3. Prepare and verify fixes for supported targets, including regression tests where practical.
4. Prepare remediation guidance and temporary mitigations where useful.
5. Coordinate remediation and disclosure with the reporter and affected customers, users, maintainers, vendors, or distributors when necessary.
6. Deploy or release fixes before or alongside public disclosure whenever practical.
7. Publish an advisory and request a CVE when appropriate.

For public repositories where GitHub Security Advisories are available, a GHSA may be used to coordinate and publish the advisory.

For proprietary products and services, remediation may be deployed directly without publishing implementation details that could create unnecessary risk for customers or systems still awaiting remediation.

## Coordinated Disclosure

We support coordinated disclosure.

Please keep vulnerability details private until a fix or mitigation is available and disclosure timing has been coordinated.

Disclosure timing depends on:

- Severity
- Exploitability
- Scope
- Fix complexity
- Deployment requirements
- Customer or downstream impact
- The time reasonably required for affected parties to update or mitigate the issue

We may request a limited embargo when necessary to reduce risk while fixes or mitigations are deployed.

We credit reporters by name or handle when appropriate unless anonymity is requested.

## Responsible Testing

- Test only against systems, data, environments, and accounts you own or are explicitly authorized to test
- Do not access, modify, copy, or exfiltrate real data beyond what is strictly necessary to demonstrate the issue
- Do not intentionally disrupt services, degrade availability, or affect other users
- Do not perform denial-of-service or resource-exhaustion testing without explicit authorization
- Respect rate limits and applicable legal boundaries
- Prefer local, isolated, staging, or disposable test environments where available
- Do not use social engineering, phishing, physical intrusion, or attacks against Aserno employees, contractors, customers, or suppliers
- If you inadvertently access sensitive data, stop testing, retain only the minimum information necessary to report the issue, and report it privately

## Safe Harbor

Aserno ApS will not pursue or support legal action for good-faith security research that:

- Follows this policy
- Is conducted against systems the researcher is authorized to test
- Avoids privacy violations and intentional service disruption
- Does not exploit a vulnerability beyond what is reasonably necessary to demonstrate it
- Reports findings privately
- Provides Aserno ApS a reasonable opportunity to investigate and remediate the issue
- Does not publicly disclose vulnerability details before coordinated disclosure

This safe harbor does not authorize testing against third-party systems, customer environments, data, or accounts that you do not have permission to access.

Compliance with this policy does not grant authorization from third parties.

## Contact

- Security reports: **security@aserno.com**
- Non-security bugs and support questions: Use the relevant repository's normal issue or support channel

_Thank you for helping keep Aserno software, services, and users safe._