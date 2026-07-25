# Security Policy

## Supported versions

Security support is prioritised as follows:

| Version | Support status |
|---|---|
| Latest stable release | Supported |
| Previous stable release | Temporary transition support where announced |
| Release candidate | Best-effort testing support |
| Alpha or beta release | Best-effort only |
| Older or superseded builds | Not supported |

A security update may increase the minimum supported client version and require users to update before signing in.

## Reporting a vulnerability

Do **not** report security vulnerabilities through a public GitHub issue, discussion, stream, social-media post or public chat.

Use one of these private methods:

1. Open this repository's **Security** tab and use **Report a vulnerability** if private vulnerability reporting is enabled.
2. If that option is unavailable, use the private contact method published on the official Streemrz website and clearly mark the message:

```text
SECURITY REPORT — STREEMRZ DOJO
```

Include:

- the affected Streemrz Dojo version;
- the affected operating system;
- a clear description of the vulnerability;
- reliable reproduction steps;
- expected and actual behaviour;
- potential impact;
- proof-of-concept material that does not expose unrelated user data;
- whether the issue is already being exploited publicly.

Never include real user access tokens, passwords, private messages, payment credentials or unrelated personal data.

## Response targets

These are response targets, not guarantees:

| Stage | Target |
|---|---:|
| Acknowledgement | Within 3 business days |
| Initial triage | Within 7 business days |
| Status update for a confirmed issue | At least every 14 days |
| Critical mitigation | As soon as reasonably possible |
| Public disclosure | After a fix or agreed disclosure date |

Complex issues, third-party dependencies and coordinated disclosure may require additional time.

## Responsible disclosure

Researchers are asked to:

- make a good-faith effort to avoid privacy violations and service disruption;
- test only with accounts and systems they own or are authorised to use;
- avoid denial-of-service testing;
- avoid accessing, modifying or deleting other users' information;
- stop testing once sensitive information is encountered;
- provide reasonable time for investigation and remediation;
- keep the report private until an agreed disclosure date;
- comply with applicable law.

Do not attempt social engineering, physical attacks, credential theft, payment fraud or attacks against third-party services.

## Scope guidance

Security-relevant areas may include:

- Streemrz OAuth and desktop callback handling;
- encrypted local session storage;
- installer and automatic-update integrity;
- Dojo backend authentication and authorisation;
- protected attachment access;
- messaging and reaction permissions;
- voice, video and screen-sharing permission boundaries;
- Tier entitlement enforcement;
- unsafe external navigation;
- remote-code execution or privilege escalation.

The following are generally not treated as vulnerabilities by themselves:

- reports requiring an already compromised device;
- missing security headers without demonstrated impact;
- self-XSS;
- outdated browser compatibility data;
- unsigned alpha-build warnings that are already documented;
- denial-of-service tests performed without written authorisation;
- social engineering;
- feature requests or ordinary product defects.

## Release integrity

Official binaries are distributed through this repository's GitHub Releases.

Each release should include a SHA-256 manifest. Users should verify downloaded installers before execution.

A mismatched hash, unexpected publisher, altered filename or binary obtained from an unofficial source should be treated as suspicious.

## Disclosure and credit

With the researcher's permission, Streemrz may acknowledge a valid report in release notes or a security advisory.

Credit may be withheld when disclosure was irresponsible, user information was exposed unnecessarily, or applicable law or contractual obligations prevent acknowledgement.

## Safe harbour intent

Streemrz intends not to pursue legal action against good-faith research that follows this policy, stays within authorised scope, avoids harm, and is reported privately.

This statement does not authorise activity against third-party infrastructure or override applicable law.
