# EDARIT Trace Pro Community Runtime 0.5.0 Beta 1

## Release type

Public beta prerelease preparation. This release has not been published; the binaries are not currently available from GitHub Releases. Publication requires separate operator authorization and approval of the beta terms.

## Highlights

- Free Community Runtime for importing trusted signed Trace Packs and scanning searchable PDF files.
- Signed fictional Demo Pack and three fictional sample PDFs.
- Scan, Process, and Batch workflows with annotated PDF plus TXT/CSV evidence.
- Consumer Runtime only; it does not create or edit Trace Packs.

## Included work

- WP-08 — Commercial Trace Pack Validation.
- DS-08.7A — Debian Community Runtime Distribution.
- DS-08.7B — Windows Community Runtime Distribution.
- DS-08.7C.1 — Public Distribution Repository Preparation.
- DS-08.7C.2 — Public Community Runtime Beta Release preparation.

## Installation and launch

See the [Windows and Debian Quick Start](docs/QUICKSTART.md). These instructions point to the intended release assets; links become usable only after separately authorized publication.

## Validation evidence

- Private source build SHA recorded by both platform checkpoints: `5ab2817104c9742724e2c2cbffecd9c0f4ada951`.
- Windows EXE/ZIP identities were recomputed from recovered artifacts; ZIP inventory, embedded hashes, and forbidden-content filename scan passed. Same-artifact Windows GUI and packaged checks are reused from DS-08.7B; GUI acceptance was operator-observed, not automated.
- Corrected Debian DEB identity and embedded file hashes were recomputed. Debian package metadata and inventory passed inspection on Windows. Debian native installation and GUI acceptance are reused from the operator-reported corrected-candidate checkpoint, not independently repeated here.
- The Debian corrected package was recorded as using packaging-only `--hidden-import PIL._tkinter_finder`; the tracked recipe at the common source SHA is unchanged. See [canonical artifact evidence](checksums/EXPECTED_ARTIFACTS.md).
- Actual production-signed synthetic Pack acceptance is recorded for Windows. It is not demonstrated for the corrected Debian artifact.
- No reproducible-build or code-signing claim is made. GitHub Actions were not required or used.

## Known limitations

- Input PDFs must contain searchable text. OCR is not included.
- Match quality depends on the imported Pack and PDF text/layout.
- Outputs require human review and are not a legal, accounting, compliance, academic, or other professional certification.
- Windows may show SmartScreen because the executable is not code-signed.
- Beta terms and the licensing status of bundled third-party components require operator review before binary publication.

## Supported platforms

- Windows x64.
- Debian amd64.

## Intended release assets

The exact file identities are recorded in [`checksums/SHA256SUMS.txt`](checksums/SHA256SUMS.txt). This PR does not contain binary payloads and does not publish them.

## Upgrade notes

Not applicable. This is a beta release preparation; prior-version upgrade behavior is not established here.
