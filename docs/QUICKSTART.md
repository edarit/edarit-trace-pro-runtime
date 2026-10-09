# Trace Pro Community Runtime — Quick Start

This guide is for Runtime `0.5.0-beta.1` and its fictional, searchable PDF samples. The signed Demo Pack is available in this repository. Windows and Debian release assets are staged but not publicly downloadable until the prerelease is separately authorized and published; beta terms and third-party licensing review remain pending.

## Windows x64

After the authorized prerelease is published, download the [Windows x64 ZIP](https://github.com/edarit/edarit-trace-pro-runtime/releases/download/v0.5.0-beta.1/EDARIT-Trace-Pro-Runtime-0.5.0-beta.1-win64.zip) and extract it to a folder you can write to:

1. Start `EDARIT-Trace-Pro-Runtime-0.5.0-beta.1-win64.exe`.
2. Download [the signed Demo Pack](../demo/invoice-po-lite-demo.tracepack) and choose **Import Pack**. Confirm the Runtime shows **Demo trusted**.
3. Download [the Alpha sample PDF](../samples/01_known_po_alpha.pdf) and choose **Open PDF**.
4. Choose **Scan PDF** to preview the invoice number, PO number, and vendor matches.
5. Choose **Process PDF** and save to a new location. Reopen the saved PDF to inspect the highlights and labels; review its TXT/CSV evidence too.
6. To process a folder, choose **Batch**, select an input folder, and choose a different output folder.

## Debian amd64

After the authorized prerelease is published, download the [Debian amd64 package](https://github.com/edarit/edarit-trace-pro-runtime/releases/download/v0.5.0-beta.1/edarit-trace-pro-runtime_0.5.0~beta1-1_amd64.deb):

1. Install it from the directory containing the downloaded package:

   ```sh
   sudo apt install ./edarit-trace-pro-runtime_0.5.0~beta1-1_amd64.deb
   ```

2. Start the application from your desktop launcher or run `edarit-trace-pro-runtime` in a terminal.
3. Download [the signed Demo Pack](../demo/invoice-po-lite-demo.tracepack) and choose **Import Pack**. Confirm **Demo trusted**.
4. Download [the Alpha sample PDF](../samples/01_known_po_alpha.pdf) and choose **Open PDF**.
5. Choose **Scan PDF**, then **Process PDF**. Save to a new location, reopen the result, and review its highlights, TXT, and CSV evidence.
6. Use **Batch** to process a folder into a separate output folder.

## What the Demo shows

The Demo has three simple detections and one exact lookup against fictional reference data embedded in the Pack. The third PDF uses a PO number absent from that fictional list; the resulting lookup evidence records that absence without making a business decision.

For detailed workflows, see the [User Guide](USER_GUIDE.md). For matching limitations, see [Known Limitations](KNOWN_LIMITATIONS.md).
