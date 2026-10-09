# EDARIT Trace Pro Community Runtime

## Free PDF processing with trusted Trace Packs

EDARIT Trace Pro Community Runtime is a free desktop application for processing text-searchable PDF files with trusted Trace Packs. It can find configured text, highlight and annotate matches, consult a Pack's configured reference data, and save reviewable PDF, TXT, and CSV evidence.

The Community Runtime runs existing Packs. It does not create or edit them. A Pack defines which checks are performed, so review the results and make sure the Pack fits your documents.

## What is Trace Pro?

Trace Pro helps people repeat configured document checks and keep evidence of what the software found. It processes PDFs; it does not make legal, accounting, compliance, academic, or other professional decisions.

## What can it do?

- Open searchable PDFs and preview configured matches.
- Process one PDF to a new, annotated PDF and TXT/CSV evidence files.
- Batch-process a folder of PDFs to a separate output folder.
- Import a trusted signed `.tracepack` file.

## Windows and Debian support

The `0.5.0-beta.1` Community Runtime candidates were validated on Windows x64 and Debian amd64. See the [Quick Start](docs/QUICKSTART.md) and [User Guide](docs/USER_GUIDE.md) for the platform-specific workflow.

## Download status

**Windows and Debian beta downloads are being prepared.** Download links will be available in this repository's GitHub Releases after a separate Release Cycle. No EXE, DEB, or ZIP download is published yet. This repository currently provides documentation and fictional Demo materials.

## Try the Demo

The signed Demo Pack and three fictional sample PDFs are available here:

- [Signed Demo Pack](demo/invoice-po-lite-demo.tracepack)
- [Known PO sample — Alpha](samples/01_known_po_alpha.pdf)
- [Known PO sample — Beta](samples/02_known_po_beta.pdf)
- [Unlisted PO sample](samples/03_unknown_po.pdf)

The Demo uses three simple detections and one fictional exact-reference lookup. The reference workbook is embedded in the signed Pack; no separate workbook is needed. Follow the [Quick Start](docs/QUICKSTART.md) after downloading a Runtime distribution.

## Understand the results

Scanning previews matches. Processing writes a new PDF with visible highlights and labels, plus TXT and CSV evidence. Batch processing writes per-file outputs and a summary. Keep outputs separate from source files and review the processed documents and evidence yourself.

## Trusted Pack model

The Community Runtime accepts trusted signed `.tracepack` files. The Demo is identified as `TRUSTED_DEMO`; EDARIT production Packs use `TRUSTED_SIGNED`. The Runtime rejects unsigned JSON Packs. A valid signature confirms the registered issuer and package integrity; it does not prove that a Pack's rules are correct for your documents.

## Community Runtime limitations

The Runtime requires text-searchable PDFs and does not include OCR. It executes the checks configured in an imported Pack and has no Pack authoring or editing controls. Document layouts can affect matching. Outputs require human review. See [Known Limitations](docs/KNOWN_LIMITATIONS.md).

## Request a Custom Trace Pack

If your documents need different checks, read [Request a Custom Trace Pack](docs/CUSTOM_PACK_REQUEST.md) and use the [public request form](https://github.com/edarit/edarit-trace-pro-runtime/issues/new/choose) for a sanitized problem description only. **Do not attach documents, workbooks, personal information, or confidential business data to a public issue.**

## Report a problem

Use the [public bug report form](https://github.com/edarit/edarit-trace-pro-runtime/issues/new/choose). Include the Runtime version, operating system, reproduction steps, and a sanitized description. Do not attach PDFs, crash dumps, or other sensitive material.

## Beta notice

This is beta software. Matching depends on the supplied Pack and the PDF layout. Review all output before relying on it. No legal, accounting, compliance, or other professional certification is provided.

## Terms

See [TERMS.md](TERMS.md). **Terms review is required before any beta binary release.** No binary release is currently available.
