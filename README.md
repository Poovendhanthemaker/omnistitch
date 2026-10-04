<img src="omnistitch-logo-256.png" width="96" alt="OmniStitch logo">

# OmniStitch

Stitch planar gamma-camera spot images into a single whole-body scintigram and export it as an NM Whole Body DICOM.

**Live:** https://stitch.nmcalc.com · part of [NMCalc](https://www.nmcalc.com)

## What it does
- Places each spot from the table position recorded in its DICOM header, so anterior and posterior line up at the same body level.
- Uses only the detector's real field of view and cross-fades the overlaps, so seams don't show bright bands.
- Matches counts between spots (acquisition time and decay correction from the radionuclide in the header).
- Sets lateral and oblique views aside by default, with an option to stitch them as their own views.
- Handles spots acquired at different zoom by resampling them to the lowest zoom (counts preserved).
- Keeps the natural noise texture across overlaps, so seams don't show as smoother bands.
- Exports a multi-frame NM Whole Body DICOM that keeps the original patient and study. Optionally, load a whole-body DICOM from your own camera to copy its vendor header layout for better compatibility with vendor software.

## Privacy
Everything runs locally in your browser. No images are uploaded anywhere.

## Use
Open the page, drop the spot DICOM files (or a folder), check the seams, and download the DICOM or a PNG. Supports uncompressed DICOM (explicit or implicit VR little endian).

## Disclaimer
For research and education. Check every stitched image against the source spots before clinical use.

Made by [Poovendhan Mathiyazhagan](https://www.linkedin.com/in/poovendhan-mathiyazhagan/).
