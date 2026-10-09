# Trace Pro Community Runtime — Quick Start

This guide is for Runtime `0.5.0-beta.1` and its fictional, searchable PDF samples. The signed Demo Pack is available in this repository; Windows and Debian Runtime downloads are being prepared and are not published yet.

## Windows x64

After the Release Cycle publishes the Windows distribution:

1. Download the Windows x64 ZIP from this repository's GitHub Releases and extract it to a folder you can write to.
2. Start `EDARIT-Trace-Pro-Runtime-0.5.0-beta.1-win64.exe`.
3. Download [the signed Demo Pack](../demo/invoice-po-lite-demo.tracepack) and choose **Import Pack**. Confirm the Runtime shows **Demo trusted**.
4. Download [the Alpha sample PDF](../samples/01_known_po_alpha.pdf) and choose **Open PDF**.
5. Choose **Scan PDF** to preview the invoice number, PO number, and vendor matches.
6. Choose **Process PDF** and save to a new location. Reopen the saved PDF to inspect the highlights and labels; review its TXT/CSV evidence too.
7. To process a folder, choose **Batch**, select an input folder, and choose a different output folder.

## Debian amd64

After the Release Cycle publishes the Debian package:

1. Download `edarit-trace-pro-runtime_0.5.0~beta1-1_amd64.deb` from this repository's GitHub Releases.
2. Install it from the directory containing the downloaded package:

   ```sh
   sudo apt install ./edarit-trace-pro-runtime_0.5.0~beta1-1_amd64.deb
   ```

3. Start the application from your desktop launcher or run `edarit-trace-pro-runtime` in a terminal.
4. Download [the signed Demo Pack](../demo/invoice-po-lite-demo.tracepack) and choose **Import Pack**. Confirm **Demo trusted**.
5. Download [the Alpha sample PDF](../samples/01_known_po_alpha.pdf) and choose **Open PDF**.
6. Choose **Scan PDF**, then **Process PDF**. Save to a new location, reopen the result, and review its highlights, TXT, and CSV evidence.
7. Use **Batch** to process a folder into a separate output folder.

## What the Demo shows

The Demo has three simple detections and one exact lookup against fictional reference data embedded in the Pack. The third PDF uses a PO number absent from that fictional list; the resulting lookup evidence records that absence without making a business decision.

For detailed workflows, see the [User Guide](USER_GUIDE.md). For matching limitations, see [Known Limitations](KNOWN_LIMITATIONS.md).
