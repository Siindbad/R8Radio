## Important

- R8Radio is in beta testing right now
- Recommended to run app as Administrator
- Change in-game Custom UDP to: `18890`
- This test is for vanilla Run8 only (`Barstow/Yermo - Needles - Mojave`)

# R8Radio

R8Radio is a desktop companion app for Run8 Train Simulator that helps bring railroad radio chatter to your session in a simple and readable way.

It detects your current Run8 session, reads your in-game location, and follows your movement so the app can stay focused on the right radio territory as you travel. The goal is to give players a cleaner, more immersive radio experience by bringing broadcast-style railroad chatter into the game, without turning the app into something complicated to use.

## What It Does

- Detects your Run8 session from local game data
- Shows current train identity and route context
- Follows town-to-town travel progression
- Tracks region and handoff flow as you move
- Supports live radio feed playback in a compact desktop app
- Includes simple in-app settings for Run8 path detection

<p align="center">
  <img src="./assets/r8radio-feature-highlight-v3-draft.png" alt="R8Radio feature highlight" width="920" />
</p>

## Roadmap

Current planned addon and feature order:

1. BNSF/UP Cajon Sub
2. BNSF San Bernardino Sub
3. BNSF Seligman Sub West
4. BNSF Bakersfield Sub
5. BNSF-UP Fresno to Modesto
6. Railway Guide
7. Railway Map

Branch-focused routes such as Arvin, Oak Creek, Lone Pine, and Trona remain lower priority than the mainline expansion path above.

## Changelogs

### Version 1.1

- Added Pre-Flight Loader
- Added More OTTO Sound Files
- Added Multi Display Support
- Fixed Some UDP Issues

## Verification suite

Current release verification order:

1. **Build + publish smoke test** : confirms the release artifact is created cleanly and the app opens as expected.
2. **Microsoft Artifact Signing** : signs the Windows app and installer executables.
3. **NuGet vulnerability audit** : checks the project packages for known vulnerable dependencies before release.
4. **BinSkim** : checks the published Windows binaries for security-oriented binary issues.
5. **Microsoft Defender CLI** : preflight scan for the release build before publish.
6. **SHA-256 checksum** : release integrity reference for the shipped file.

## License

MIT License. Copyright (c) 2026 Jason Jorgensen.
