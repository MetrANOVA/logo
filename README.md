# MetrANOVA Logo

![MetrANOVA Logo](parts.svg)

This is a version of the MetrANOVA logo rendered as Scalable Vector
Graphics (SVG).

The font used is [Microsoft Terbuchet
MS](https://learn.microsoft.com/en-us/typography/font-list/trebuchet-ms),
which is proprietary and requires Windows or a Mac with Microsoft
Office installed.


## Prerequisites

Building the logo requires a system with the following available at
the command line:

 * ImageMagick
 * Inkscape
 * Make
 * Tar
 * Xsltproc
 * Zip

On Red Hat, `yum -y install ImageMagick inkscape make tar libxslt zip` will
install everything needed.


## Building the Logo

Run `make` 


## Modifying the Logo

The original, complete version of the logo is `original.svg`.

It was created in Inkscape, and edits should be done there as well.
The files contain Inkscape-specific XML but should still work fine
with anything that wants to render it.

Because there's no easy, practical way to automatically derive
versions of the logo with proper bounding boxes and margins and text
converted to paths, the repository includes files where this has been
done.

**If the logo is changed, follow this procedure to update the files:**

 * Start Inkscape
 * Open `original.svg`
 * Select all text objects
 * Convert them to paths (`Shift` + `Ctrl` + `C`)
    * **DO NOT SAVE `original.svg` AFTER THIS POINT.**
 * Make all layers visible
 * Open _Document Properties_ (`Shift` + `Ctrl` + `D`)
 * Expand _Resize page to content...`
 * Make sure all four margins are set to `15.0`.
 * Click _Resize page to drawing or selection_.
 * Save as `parts.svg`.
 * Make the `powered` layer invisible.
 * Click _Resize page to drawing or selection_ in _Document Properties_.
 * Save as `parts-text.svg`.
 * Make the `text` layer invisible.
 * Click _Resize page to drawing or selection_ in _Document Properties_.
 * Save as `parts-icon.svg`.
 * Quit Inkscape
