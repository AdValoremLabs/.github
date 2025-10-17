# Contributing to Ad Valorem Labs

Thanks for wanting to improve our kits and documentation!  
Whether you're fixing a typo, adding a script, or refining instructions — contributions are welcome.

---

## 🧱 Ground rules

- Keep your changes **modular and documented**.  
  If you update a script, confirm it runs on a clean flash of the kit image.
- Use **pull requests** against the `develop` branch.  
  The `main` branch is for release-ready code only.
- Add or update notes in `CHANGELOG.md` when you make a functional change.

---

## 🧾 Commit message format

We use **[Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)** for clarity and automated changelogs.

Format:
type(scope): short description

Examples:
feat(ha): add Wi-Fi my-network template
fix(proxmox): correct NVMe mount path
docs(retropie): update controller pairing steps
chore: refresh QR codes


Common types:
- **feat** – new feature or enhancement  
- **fix** – bug or error correction  
- **docs** – documentation only  
- **chore** – maintenance, formatting, housekeeping  
- **refactor** – internal changes without functional difference  
- **test** – adding or updating tests/workflows

---

## ✅ Pull request checklist

Before opening a PR:
- [ ] Run the changed scripts on a fresh kit image.
- [ ] Update or verify quickstart and troubleshooting docs.
- [ ] Add notes to `CHANGELOG.md`.
- [ ] Verify Markdown links (`.github/workflows/markdown-link-check.yml` will also do this).
- [ ] Confirm the build jobs pass (ShellCheck, link check, QR build, etc).

---

## 🧠 Style & tone

- Write docs in plain, friendly English.  
  Assume the reader is capable but new to the specific kit.
- Keep Markdown readable in raw form — don’t overuse HTML.

---

## 💬 Questions or issues?

If you’re not sure where to start, open a **Discussion** or file an issue in the  
[help-desk](https://github.com/AdValoremLabs/help-desk) repo.

Thanks for helping us make these kits cleaner, clearer, and more useful.
