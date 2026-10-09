# 0.5.0-beta.1 Canonical Artifact Evidence

This file records release-preparation evidence. The artifacts remain local and are not published. The machine-readable release asset checksums are in [`SHA256SUMS.txt`](SHA256SUMS.txt).

## Common source and build provenance

- Private source repository: `edarit/edarit-trace-pro` (read-only for this release preparation).
- Common private build-source SHA recorded by the platform checkpoints: `5ab2817104c9742724e2c2cbffecd9c0f4ada951`.
- Public documentation repository baseline after PR #1: `23fd6edd0a294ce410a47ed6ad93b9b61a8dd4f5`. Public and private SHAs belong to separate repositories and are not compared as one lineage.
- Windows build command recorded in DS-08.7B: `packaging/windows/build_runtime.ps1`; Windows artifact hashes were independently recomputed from the recovered files.
- Debian corrected candidate: the exact `.deb` was recovered and independently checked. The operator checkpoint records the same common source SHA and an additional packaging-time PyInstaller option, `--hidden-import PIL._tkinter_finder`, to fix the packaged PDF preview. The tracked recipe at the common source SHA is `packaging/debian/build_runtime.sh`; that committed script does not contain the added option. The correction is an invocation-level packaging argument, not a source edit. For a future rebuild, apply that argument to the script's PyInstaller invocation and preserve the source commit unchanged. No rebuild was performed during this release preparation.
- Earlier DS-08.7A repository records identify a superseded pre-preview-fix Debian artifact and a different source SHA. That older artifact is not selected for this release set; the corrected-candidate checkpoint and the physically recovered corrected DEB are the evidence used here.
- The exact Debian build log was not present on this Windows host. Source and packaging lineage above distinguish the operator checkpoint's build record from what was independently inspected here.

## Verified asset identities

| Asset | Size | SHA-256 | Verification |
|---|---:|---|---|
| `EDARIT-Trace-Pro-Runtime-0.5.0-beta.1-win64.exe` | 39,242,935 bytes | `052c7424cbd047220e8b68f8a06fe2aa2cc5c5042bcc3af218ed95061f4ca17f` | Recomputed on recovered EXE and ZIP-contained copy. |
| `EDARIT-Trace-Pro-Runtime-0.5.0-beta.1-win64.zip` | 38,827,953 bytes | `9243d4ff129de8e7f8bead0dc0c06ffaa14558622ec270ac1acc7b836bf6fff2` | Recomputed; nine entries; all eight `SHA256SUMS.txt` entries verified; no forbidden filename matches. |
| `edarit-trace-pro-runtime_0.5.0~beta1-1_amd64.deb` | 44,873,140 bytes | `62f2f30e115ccdd1a6ecf483f086102a9ed4de39dba3916b10001024916db6ae` | Recomputed; Debian format 2.0; package/version/architecture verified; package's eight file checksums verified. |
| `invoice-po-lite-demo.tracepack` | 4,522 bytes | `44f31edd5865fdc6575b983055afc0d703f59a1df218e86c7b9ea9d3e25b9dcb` | Recomputed; matches the Pack embedded in the Debian package and published repository file. |

The Debian package metadata is `edarit-trace-pro-runtime`, version `0.5.0~beta1-1`, architecture `amd64`, with runtime dependencies `libc6` and `libstdc++6`. Its 17-entry payload contains the Runtime binary, signed Demo, three fictional sample PDFs, public docs, and checksum list. No Studio, Pack Factory, signing utilities, private-key files, or internal acceptance files were found. Package installation and GUI validation were not repeated on Windows; the Debian-native checkpoint is operator-reported evidence.

## Reused platform acceptance

Windows DS-08.7B operator-observed GUI evidence and same-artifact packaged acceptance are reused because the EXE and ZIP identities match exactly. The GUI was not computer-automated. The Debian corrected-candidate checkpoint reports native GUI Demo trust, Alpha PDF preview, three Scan matches, Process, and Batch PASS; those native interactions were operator-reported, not independently observed in this Windows session. The corrected Debian checkpoint did not demonstrate an actual production-signed Pack test on the packaged Debian Runtime. The active release preparation does not represent that test as passed; if the release gate requires it, it remains a pre-publication action.

## Security and publication boundary

- Only the versioned checksums and evidence in this document are committed. EXE, ZIP, DEB, and Demo release payloads are staged outside this Git repository.
- The public Git history is independent from the private source history.
- The Runtime is proprietary/freeware beta and this public repository does not grant an open-source license to the Runtime.
- Terms approval is pending. No tag, binary upload, or public release is authorized by this preparation PR.
