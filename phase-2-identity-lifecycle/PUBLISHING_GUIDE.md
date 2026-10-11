# Publish Phase 2 to GitHub

1. Review the 26 screenshots for personally identifying details before uploading to a **public** repository. Redact locally if necessary.
2. Open your existing IAM portfolio repository on GitHub (or create a new one).
3. Choose **Add file → Upload files**. GitHub’s web uploader does not preserve folders when you upload a ZIP as a single file. Instead, unzip this package locally, then drag the entire `phase-2-identity-lifecycle` folder into the uploader if your browser supports folder drag-and-drop. Alternatively, use GitHub Desktop or Git.
4. Ensure the files appear under `phase-2-identity-lifecycle/`, including `screenshots/`.
5. Enter a commit message such as `docs: add Phase 2 Entra ID JML portfolio lab` and commit.
6. Open `phase-2-identity-lifecycle/README.md` on GitHub; check all embedded screenshots and the evidence index links.
7. Add a link in the repository root README: `[Phase 2 — Identity Lifecycle Management](phase-2-identity-lifecycle/README.md)`.

**If using Git locally:**

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
cd YOUR_REPOSITORY
# Copy the extracted phase-2-identity-lifecycle folder here
git add phase-2-identity-lifecycle
git commit -m "docs: add Phase 2 Entra ID JML portfolio lab"
git push
```

Do not upload the ZIP file itself as your portfolio content: GitHub cannot display its internal README and image links as a navigable folder.
