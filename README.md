# Intercare Therapy — Email Signature

Self-serve installer for the official Intercare Therapy Outlook email signature.

**👉 Open the installer:** https://YOUR-ORG.github.io/email-signature/

---

## For staff — how to set up your signature

1. Open the installer link above.
2. Fill in your **name, job title, phone, and email**.
3. Click **Copy signature**.
4. In Outlook, go to **Signatures**, click **New**, paste, and save:
   - **Windows (classic):** File → Options → Mail → Signatures
   - **Windows (new Outlook):** Settings → Accounts → Signatures
   - **Mac:** Outlook → Settings → Signatures
   - **Web:** Settings (gear) → Mail → Compose and reply
5. Set as the default for **new messages** and **replies/forwards**.

If your browser blocks the copy button, use the **Download .htm file** button on the installer instead — open the downloaded file, select all, copy, and paste into Outlook.

---

## For admins — updating the signature

This repo serves one file: `index.html`. The Intercare logo, colors, HQ ribbon, and confidentiality footer are baked into that file as a single self-contained HTML page (no external dependencies, no CDN, no hosting required beyond Pages itself).

To make changes:

1. Edit `index.html` directly in GitHub (pencil icon) or via PR.
2. Commit to `main`. GitHub Pages redeploys within ~1 minute.
3. Staff don't need to do anything — they just refresh the page next time they install.

### What's in `index.html`
- The installer UI (form on the left, live preview on the right, copy/download buttons).
- The signature template itself (an Outlook-compatible HTML table with the logo inlined as base64).
- Step-by-step install instructions for Windows / Mac / Web Outlook.

### Common changes
| Change | Where in `index.html` |
|---|---|
| HQ address or "New HQ" ribbon copy | Search for `Headquarters` and `New HQ` |
| Confidentiality / HIPAA footer | Search for `WARNING:` |
| Brand colors (navy `#291a6b`, teal `#26cca0`) | Search for the hex codes |
| Default placeholder values | Search for `Ashley Quintero` |

---

## Hosting (GitHub Pages)

This repo is deployed via **Settings → Pages → Branch: `main` / root**. No build step — Pages serves `index.html` directly.

---

## License / ownership

© Intercare Therapy, Inc. Internal brand asset. Do not redistribute outside the organization.
