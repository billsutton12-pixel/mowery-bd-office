# Mowery BD Office — Cowork marketplace

This repository is a Claude plugin marketplace containing one plugin, `mowery-bd-office` — Bill Sutton's five-agent BD crew (Scout, Chase, Quill, Sage, Ace).

## Publish (one time)

1. Create a **new public** repository on GitHub (e.g. `mowery-bd-office`). It must be public — Cowork reads it from an unauthenticated session.
2. Upload the contents of this folder so that `.claude-plugin/marketplace.json` sits at the **repository root** (not inside a subfolder). Two ways:
   - **GitHub web**: on the empty repo page, click "uploading an existing file," then drag in the `.claude-plugin` folder and the `plugins` folder together.
   - **Git CLI**:
     ```
     cd mowery-mkt
     git init && git add . && git commit -m "Mowery BD Office marketplace"
     git branch -M main
     git remote add origin https://github.com/<you>/mowery-bd-office.git
     git push -u origin main
     ```

## Install in Cowork

1. Open the Claude desktop app → **Cowork** tab.
2. Left sidebar → **Customize** → **Plugins** → the **"+"** button → **Add marketplace from GitHub**.
3. Enter your repo as `your-github-username/mowery-bd-office` (or the full https URL).
4. Once it syncs, open the marketplace, find **mowery-bd-office**, and click **Install**.
5. Open the installed plugin and make sure Scout, Chase, Quill, Sage, and Ace are enabled.

Then connect HubSpot, Outlook/Microsoft 365, and Google Drive in Cowork, and dispatch by call sign: `Chase, which deals need a touch this week?`

## What's inside

```
.claude-plugin/marketplace.json      <- lists the plugin
plugins/mowery-bd-office/
  .claude-plugin/plugin.json          <- plugin manifest
  skills/                             <- Scout, Chase, Quill, Sage, Ace
  README.md
```
