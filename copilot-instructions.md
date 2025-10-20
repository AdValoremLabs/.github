<!--
  .github/copilot-instructions.md
  Purpose: Short, actionable guidance for AI coding agents working in this org-level repo.
-->
# Copilot instructions — AdValoremLabs org-level repo

Keep edits small and consistent with existing kit patterns. This repository is a collection
of organization-level kits and templates (see top-level directories: `home-assistant/`,
`proxmox/`, `retropie/`, `pwnagotchi/`, `advaloremlabs/`, and `advaloremlabs.github.io/`).

Key points for productive changes
- Big picture: this repo contains reusable kit templates and org-wide GitHub automation.
  - Kits follow a consistent structure: a `README.md`, `BRANDING.md`, `LICENSE` and
    `LICENSE.docs`, `TRADEMARK.md`, and a `docs/` folder for supplemental content.
  - GitHub Pages content lives under `advaloremlabs.github.io/` and is consumed by
    the org website. Changes there affect published pages.

- Where to look (examples)
  - README template: `.github/README.md` — use this when creating new kit READMEs.
  - CI/workflows: `.github/workflows/` — e.g. `.github/workflows/shellcheck.yml` uses
    `actions/checkout@v4` and `ludeeus/action-shellcheck@v2` for linting shell scripts.
  - Top-level scripts: `scripts_flash_haos.sh`, `scripts_flash_proxmox.sh` — shell scripts
    should be ShellCheck-clean and portable to WSL/Ubuntu.

- Project-specific conventions (do not invent these)
  - Every kit repo mirrors the same set of metadata files (see list above) — keep that
    layout when adding new kits or copying templates.
  - Images referenced by kit READMEs commonly live under `docs/images/` (example: QR
    image referenced in `.github/README.md`).
  - Use plain, short README sections: Overview → What’s in the Kit → First Boot → Support

- CI & local dev checks
  - CI uses GitHub Actions workflows in `.github/workflows/`. Example: shellcheck is
    executed on pushes that touch `scripts/**/*.sh` as declared in
    `.github/workflows/shellcheck.yml`.
  - Before changing shell scripts, run shellcheck locally (WSL is the expected shell).
    If you don't have shellcheck installed, use the `shellcheck` package for your distro.

- How to make safe, accepted edits
  - Preserve license headers and `LICENSE.docs` content when touching legal files.
  - When adding a new kit, copy the README template in `.github/README.md` and fill the
    short tagline and `docs/images/qr.png` if appropriate.
  - Keep changes minimal in org-level files. For workflow changes, prefer small, well-
    justified patches and reference existing workflows for consistency.

- Examples of actionable tasks for AI agents
  - Update `home-assistant/README.md` to match the `.github/README.md` template.
  - Add ShellCheck fixes to `scripts_flash_proxmox.sh` and validate with local shellcheck.
  - Add a new kit folder `my-kit/` containing `README.md`, `docs/`, `LICENSE`, and
    `BRANDING.md` following existing naming and layout.

If anything in these notes is unclear or you want more examples (for instance, a
canonical README skeleton or a checklist for adding a kit), tell me which area to
expand and I will update this file.
