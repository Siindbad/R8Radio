# Security

R8Radio is released with a simple verification gate so users can see what was checked before a public build is published.

This release flow is still being aligned, so this page is the first public-facing security baseline rather than the final long-term release policy.

## Release Verification Gate

Public releases are intended to follow this order:

1. **Build + publish smoke test**  
   Confirms the release build is created cleanly and opens as expected.

2. **Microsoft Defender CLI**  
   Used as a preflight malware/security scan before release publish.

3. **VirusTotal**  
   Used as public release evidence for the final shipped artifact.

4. **SHA-256 checksum**  
   Used as the release integrity reference for the final file.

## Verification Report Style

When the release flow is fully aligned, R8Radio release assurance will be shown in a simple Pass / Fail gate report.

Example gate rows:

- **Build + publish smoke test** : PASS / FAIL
- **Microsoft Defender CLI** : PASS / FAIL
- **VirusTotal** : PASS / FAIL
- **SHA-256** : PASS / FAIL

Additional gates may be added later as the release process matures.

## Release Artifact Rule

When release packaging is fully in place, each public GitHub Release should include a generated `security-report.txt`.

Current direction:

- release tags should match the release version
  - example:
    - `v1.0`
- `security-report.txt` should be attached to the GitHub Releases page with the matching tagged release
- `security-report.txt` should **not** be shipped inside the public app `dist/` folder

This keeps the app package focused on runtime files while the release page carries the release-assurance evidence.

## Release Page Hygiene

Planned release-flow direction:

- when a newer public release is published, the previous latest release may be removed so the public release lane stays clean and easy to follow
- the newest tagged release should remain the primary public release reference

This is a future release/publish flow note and may be refined later as the public release process matures.

## Stop-On-Fail Release Rule

Planned release-flow direction:

- the release process should be monitored stage by stage
- if any verification or report step fails, publish should stop immediately
- failed stages should be inspected and triaged before release work continues

This future monitored flow is intended to cover the full release chain, including:

- build and publish checks
- security gate checks
- release artifact verification
- upload-stage checks
- VirusTotal submission and result watch

Simple rule:

- if anything fails, stop publish
- inspect the failure
- triage the cause
- only continue after the issue is understood and resolved

## Reporting A Security Concern

If you believe you found a security issue in a public release, please report it privately through the project contact path instead of opening a public exploit-style issue first.

Until a fuller disclosure flow is modeled, use the maintainer contact listed in the public project materials.
