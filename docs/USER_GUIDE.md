# EDARIT Trace Pro Community Runtime User Guide

Trace Pro Community Runtime `0.5.0-beta.1` consumes trusted signed Trace Packs to find configured text in searchable PDFs, preview matches, and save reviewable output. It does not create or edit Packs. The prerelease assets are not yet published; terms and third-party licensing review remain pending. See the [Quick Start](QUICKSTART.md) for platform steps after publication.

## Import a Pack

Choose **Import Pack** and select a signed `.tracepack`. The Runtime shows the Pack name, version, trust status, and issuer. The included Demo is trusted as `TRUSTED_DEMO`; EDARIT production Packs use `TRUSTED_SIGNED`. Unsigned JSON Packs are rejected by the Community Runtime.

A trusted signature identifies the registered signer and detects package changes. It does not certify the Pack's rules or guarantee that they fit a particular document layout.

## Process one PDF

1. Choose **Open PDF** and select a text-searchable PDF.
2. Choose **Scan PDF** to preview the configured matches and confirm that they make sense for the document.
3. Choose **Process PDF** and save to a separate destination. Keep the source document unchanged.
4. Reopen the saved PDF and inspect the visible highlights and labels. Review the TXT/CSV evidence separately.

The evidence reports configured detections and lookup context. A missing reference entry is evidence of absence from that configured list, not an automatic pass/fail judgment.

## Batch processing

Choose **Batch**, select a folder of PDFs, and choose a different output folder. The Runtime writes one processed PDF and related evidence for each input plus a batch summary. Inspect several results, including a document with an unlisted reference value.

The consumer command-line batch path is also available after installing a Runtime distribution:

```text
edarit-trace-pro-runtime --batch INPUT_DIR --output OUTPUT_DIR --pack PACK_FILE
```

Use an input directory containing PDFs, a different writable output directory, and a trusted `.tracepack` file. Review generated output before relying on it.

## Windows

After separate publication authorization, download and extract the [Windows x64 ZIP](https://github.com/edarit/edarit-trace-pro-runtime/releases/download/v0.5.0-beta.1/EDARIT-Trace-Pro-Runtime-0.5.0-beta.1-win64.zip) to a writable folder and start `EDARIT-Trace-Pro-Runtime-0.5.0-beta.1-win64.exe`. Use the buttons described above. Windows may display a SmartScreen warning for an unsigned beta executable; see [Known Limitations](KNOWN_LIMITATIONS.md).

## Debian

After separate publication authorization, download the [Debian amd64 package](https://github.com/edarit/edarit-trace-pro-runtime/releases/download/v0.5.0-beta.1/edarit-trace-pro-runtime_0.5.0~beta1-1_amd64.deb) and install it with `sudo apt install ./edarit-trace-pro-runtime_0.5.0~beta1-1_amd64.deb`. Start `edarit-trace-pro-runtime` from the desktop launcher or terminal. A desktop environment is required for the graphical application.

## Limits

The Runtime requires searchable text and does not include OCR. It executes the checks in the imported Pack but provides no authoring controls. PDF layout differences can affect matches. Review results yourself; Trace Pro does not make legal, accounting, compliance, academic, or other professional decisions.
