# Security policy

SoroWorks tools sit close to money: SoroForge holds a deployer's signing key, and all three talk to Stellar RPC endpoints. We take reports seriously and would rather hear about a problem privately first.

## Reporting a vulnerability

**Do not open a public issue.** Use GitHub's private reporting instead: open the affected repository's **Security** tab and choose **Report a vulnerability**. Only the maintainers can see the report.

Please include what you found, how to reproduce it, and the version or commit you tested. We aim to acknowledge a report within three working days and to agree a disclosure date with you once a fix is ready.

## Supported versions

Fixes are made on `main` and shipped in the next release of the affected tool. Only the latest release is supported.

## What is in scope

Anything that could expose or misuse key material, sign or submit something the operator did not intend, bypass SoroForge's API token, or let crafted RPC responses or contract data crash a tool or mislead its output — for example a decoded interface or health verdict that does not match the chain.

Dependency vulnerabilities are scanned on every change and weekly with `govulncheck`; a report is still welcome if you find one that is reachable and we have missed it.
