# geowrite2rtf

*geowrite2rtf* is a simple tool that converts a C64/C128 GEOS GeoWrite document in [.CVT format](http://unusedino.de/ec64/technical/formats/cvt.html) into RTF format. The tool can optionally write HTML or plain-text as well, though at a loss of some or all formatting.
This fork was created because the original version didn't work for me (formatted the page in a way that only 1 character could fit in a row) with the GeoWrite files that I created with GEOS65 (GEOS128 port for the MEGA65 computer) so the conversion was a bit simplified to have this fixed.

Use a tool like [c1541](http://vice-emu.sourceforge.net/vice_12.html) or [DirMaster](http://style64.org/dirmaster) to extract the file from a D64/D71/D81/etc. disk image into a .CVT first.

## Usage

* First you need to extract the file from a D64/D71/D81 disk image into CVT format using either [DirMaster](http://style64.org/dirmaster) for Windows, or the [c1541](http://vice-emu.sourceforge.net/vice_12.html) command line tool that ships with VICE:

    geosread dOCUMENT document.cvt

* Then run *geowrite2rtf* like this to convert the CVT file to RTF:

    geowrite2rtf document.cvt document.rtf

## Status

*geowrite2rtf* supports:

* font size
* styles: underline, bold, reverse, italics, outline, superscript, subscript
* alignment: left, right, center, justified
* insets
* tab stops
* line spacing

*geowrite2rtf* discards:

* font faces
* headers, footers
* colors
* page size
* graphics

Contributions welcome!

## License

[BSD 2-Clause](http://opensource.org/licenses/BSD-2-Clause)

## Author

Michael Steil <mist64@mac.com>
