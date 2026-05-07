# Verification Report

Generated from `dist/security/security-report.txt`. Release version: `v1.4.0`.

## Security Gate Status

| Gate | Status |
| --- | --- |
| Build + publish smoke test | ![PASS](https://img.shields.io/badge/PASS-006400?style=flat-square) |
| Microsoft Artifact Signing | ![PASS](https://img.shields.io/badge/PASS-006400?style=flat-square) |
| NuGet vulnerability audit | ![PASS](https://img.shields.io/badge/PASS-006400?style=flat-square) |
| OSV Scanner | ![PASS](https://img.shields.io/badge/PASS-006400?style=flat-square) |
| Syft SBOM | ![PASS](https://img.shields.io/badge/PASS-006400?style=flat-square) |
| Grype vulnerability scan | ![PASS](https://img.shields.io/badge/PASS-006400?style=flat-square) |
| BinSkim | ![PASS](https://img.shields.io/badge/PASS-006400?style=flat-square) |
| Microsoft Defender CLI | ![PASS](https://img.shields.io/badge/PASS-006400?style=flat-square) |
| VirusTotal installer scan | ![PASS](https://img.shields.io/badge/PASS-006400?style=flat-square) |
| SHA256 | ![PASS](https://img.shields.io/badge/PASS-006400?style=flat-square) |

## Assurance Note

- Historical audit note:
  - an optional VirusTotal research pass previously showed a `Zillya` false-positive on the unsigned Windows launcher EXE
  - the packaged payload without that launcher was isolated and cleared in the controlled audit lane
  - we therefore treat that remaining `Zillya` signal as a launcher-layer false positive rather than evidence of a malicious payload
