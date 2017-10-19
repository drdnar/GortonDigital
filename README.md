# GortonDigital
A revival of a 20th century interwar font.

In the early- to mid-20th century, the George Gorton Machine Company made
engraving machines (among other machines).  They also made a few typefaces that
were often used with the machines, the most common of which was simply called
Gorton.  This is a digitalization of the Gorton font family.

## Variants in the Family
The Gorton typeface was available in several fonts of varying sizes and widths,
and in an inclined variant.  Currently, I only have the normal width available.

## Digitization process
Because the Gorton font family was created by machinists, it seems reasonable to
conclude that the creator used geometric principles to draw parts of many
glyphs, especially since doing so would presumably make fabrication easier.  It
also seems likely the creator was familiar with conic sections.  Consequently,
most of the uppercase glyphs and many of the lowercase and numeral glyphs were
measured, not traced; that is, I measured properties like line angle, curve
radius, and width-to-height ratio to derive coordinates for control points i
the glyphs.

Nevertheless, some glyphs, such as the six, did not match simple curves very
well.  Additionally, while form 2553 from the Gorton archive site had
a good decent-resolution photo of the uppercase glyphs, there wasn't a good
resolutions photo of the lowercase glyphs.  Therefore, the lowercase glyphs
are not as good a match, and could still use some work if I had access to
better pictures.

## Notes on Specific Glyphs
TODO

## Creating the Output Fonts from the Template
Run the generateStrokes.ff script through FontForge, e.g. fontforge generateStrokes.ff gortondigital.sdf


================================================================================
