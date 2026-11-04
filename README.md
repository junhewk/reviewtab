# ReviewTab

A privacy/local-first, medical-centered reviewer-support workspace for confidential journal peer review.

**This app is not an independent AI reviewer.** Human interpretation, editing, selection, adoption and rejection of suggestions are the intended workflow. Keeping scientific and editorial judgment and responsibility with the human is a deliberate ethical and product boundary, not unfinished automation.

This repository holds release downloads and public documentation only. The app's source repository is not published here.

## Download 0.1.1

[Release notes and all assets](https://github.com/junhewk/reviewtab/releases/tag/v0.1.1)

| Platform | Download | Start |
| --- | --- | --- |
| macOS, Apple silicon (arm64) | [macOS archive](https://github.com/junhewk/reviewtab/releases/download/v0.1.1/reviewtab-0.1.1-macos-arm64.tar.gz) | Double-click `ReviewTab.command` |
| Windows, x64 | [Windows ZIP](https://github.com/junhewk/reviewtab/releases/download/v0.1.1/reviewtab-0.1.1-windows-x64.zip) | Double-click `ReviewTab.bat` |

**macOS:** Developer ID signed and notarized by Apple. Unpack the archive and confirm the normal macOS Open dialog on first launch.

**Windows:** This ZIP is **unsigned**. Smart App Control or other application-control policies may block it. Smart App Control blocked execution on the build machine, so packaged startup was not verified there. Unsigned ZIP distribution is intentional for this release; it is not a signed or Smart App Control-verified build.

Only the attached assets are available. There is no Linux archive attached to release 0.1.1. Signing status and available platforms are specific to each release; older downloads do not describe this version.

The app is compiled with Bun 1.4.3. No source checkout or separately installed Node, Bun or Python runtime is needed.

## What it supports

- **Argument:** inspect and edit source-linked argument diagrams and open review issues.
- **Section review:** choose prose checks or a quantitative, qualitative, systematic, scoping or narrative-review methodology focus, within a limited budget.
- **Citations and references:** choose local mechanical checks, approved bibliographic-record lookups or experimental deep content comparison.
- **Reviewer-owned notes and comments:** inspect source and model suggestions side by side, then adopt, revise or reject them. Export explicitly adopted comments as Markdown.

**Deep citation comparison is experimental and full-text retrieval has limitations.** Access restrictions, unreadable PDFs, images and external appendices can prevent comparison. Unavailable material remains unchecked; it is not itself evidence of a manuscript defect or fabrication.

This is focused support, not an all-round review system. It does not aim to find every error, certify medical or scientific validity, reanalyse raw data/code/transcripts, reproduce statistical calculations, automatically rewrite manuscripts or decide publication. Suggestions and diagrams can be missing or mistaken; the reviewer writes the final judgment and comments.

## Start and use

1. Download and unpack the archive for your system.
2. Open its start file from the table above. ReviewTab opens in your browser; keep the start window open while working.
3. Open a manuscript. Viewing a document and taking notes need no model.
4. Choose a model when needed. Each model task shows its scope and budget and runs only after approval.
5. Review the suggestions and source evidence, then select and edit the comments you want to include.

The app interface supports English and Korean. Review output has its own recorded language setting; quotations stay in the source language.

The server is a local, single-user workspace, not a public multi-user service. Do not expose it directly to the internet.

## Models and confidentiality

- The app accepts model endpoints on your computer or private network, or OpenRouter with zero data retention (ZDR). Other services are refused.
- An approved model task sends the required manuscript text to the selected endpoint. Approved bibliography/full-text lookups send queries to scholarly services.
- No manuscript content, usage data or telemetry is sent to the app's author.
- The reviewer decides whether a journal's confidentiality and AI-use policies permit a model or lookup.
- Browser extensions allowed to read the page can also read the manuscript. Use a browser profile appropriate for confidential work.

Local-first is not an air gap or a security certification. Model/provider configuration, deployment settings and browser extensions affect confidentiality.

## Saved work, updating and removal

Review data is stored separately from the app folder. To update, unpack a new version into a new folder; existing work remains in the data folder.

Records are kept until explicitly deleted. **Saved data** in the app provides a preview and confirmation for deleting a manuscript's local records and uploaded copies. External originals, exports, backups and other data folders are not deleted by that action. There is no automatic expiry or secure-erasure guarantee.

Do not share a data folder concurrently across machines or with older app versions. The archive's `README.txt` describes platform-specific storage locations and removal.

## Check a download

Download [SHA256SUMS](https://github.com/junhewk/reviewtab/releases/download/v0.1.1/SHA256SUMS) beside your archive. Each archive also has its own `.sha256` sidecar on the release.

For a downloaded macOS archive, place its matching `.sha256` sidecar beside it and run:

```sh
shasum -a 256 -c reviewtab-0.1.1-macos-arm64.tar.gz.sha256
```

For the Windows ZIP in PowerShell:

```powershell
Get-FileHash .\reviewtab-0.1.1-windows-x64.zip -Algorithm SHA256
```

Compare the Windows result with its entry in `SHA256SUMS`. Checksum agreement confirms the bytes match the published value; it does not by itself authenticate the publisher or certify security. No app-level signed integrity manifest is provided for this release; macOS platform signing/notarization is separate.

## Licence

ReviewTab is free to use under its own licence. Read the `LICENSE.md` bundled with your download for the terms applicable to that version. Its `THIRD_PARTY_NOTICES.txt` lists included open-source components, their licences and the relinking-material offer.
