# ClipStack releases

This is the distribution-only repository for ClipStack, a local Windows clipboard utility. Application source, private signing keys, credentials and user data do not belong in this repository.

## Install

Download the versioned **ClipStack-Setup-VERSION.exe** asset from [Releases](https://github.com/FuegoRoseAI/ClipStack-Releases/releases). Setup installs for the current Windows user without administrator privileges, includes its runtime, and preserves existing ClipStack data and settings. Close ClipStack using its tray Exit action before a manual upgrade; Setup never force-closes it.

Version 1.2.1 is the first release with this default update host. Older users must install it manually once. Then use **Settings > About > Check for updates**. Checks are manual; downloading and installation require user action.

## Update feed

Stable signed metadata: https://github.com/FuegoRoseAI/ClipStack-Releases/releases/latest/download/clipstack-stable-v1.json

Each stable release includes a version-specific installer URL, signed metadata, release notes and .NET license/third-party notices. Installers at published version URLs must not be replaced. GitHub's generated source archives contain this distribution repository, not the application source.

Metadata uses schema v1 and an RSA signature checked against ClipStack's embedded public key. Its signed payload binds version, release notes, installer URL, size and SHA-256. Metadata is time-limited and must be refreshed by the publisher before expiry. The private metadata key remains in the publisher's non-exportable Windows key store.

**Metadata signing is not Windows Authenticode signing.** The application and installer are currently Windows-unsigned. Keep Windows protections enabled and review normal Windows prompts.

All clipboard history, image assets, collections, saved sequences and user settings remain local. The updater never uploads clipboard data.
