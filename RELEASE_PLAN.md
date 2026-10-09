# EDARIT Trace Pro Community Runtime — Release Plan

## 0.5.0-beta.1 — Public Beta Prerelease

**State:** Release preparation PR; not a Release Candidate yet.
**Target:** GitHub prerelease `v0.5.0-beta.1` after separate approval.
**Public repository base:** `23fd6edd0a294ce410a47ed6ad93b9b61a8dd4f5`.
**Private artifact source:** `5ab2817104c9742724e2c2cbffecd9c0f4ada951`.

### Artifact gate

- [x] Windows x64 EXE recovered; size and SHA-256 match the canonical Windows checkpoint.
- [x] Windows ZIP recovered; size, SHA-256, inventory, and embedded file hashes verified.
- [x] Debian amd64 corrected candidate recovered; size, SHA-256, package metadata, inventory, and embedded file hashes verified.
- [x] Signed Demo Pack physically available; SHA-256 verified.
- [x] Platform checkpoints record common private source SHA `5ab2817104c9742724e2c2cbffecd9c0f4ada951`; Debian used packaging-only `--hidden-import PIL._tkinter_finder` and did not change the tracked source commit.
- [ ] Operator approves final beta-use terms.
- [ ] Operator confirms licensing coverage and required notices for bundled third-party components, including PyMuPDF/Artifex.
- [ ] If the active gate requires it, actual production-signed synthetic Pack acceptance on the corrected Debian Runtime.
- [ ] Separate authorization for merge, tag, binary upload, and public publication.

### Platform validation

Windows packaged GUI and same-artifact checks are reused from DS-08.7B. The GUI was operator-observed and was not computer-automated. Debian installation, launch, Demo trust, preview, Scan, Process, and Batch PASS are reused from the corrected-candidate operator checkpoint; this Windows session independently checked the physical DEB identity, metadata, inventory, and embedded checksums only. No actual production-signed Pack test is claimed for the corrected Debian package.

### Public boundary and delivery

Only documentation and actual asset checksums belong in Git. The four release assets remain outside the repository. GitHub Actions are not required or used. Prepare one release PR from `release/v0.5.0-beta.1`; do not merge, tag, upload assets, or publish until the gates above and separate authorization are satisfied.
