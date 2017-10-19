# GortonDigital
A revival of a 20th century interwar typeface.

In the early- to mid-20th century, the George Gorton Machine Company made
engraving machines (among other machines).  They also made a few typefaces that
were often used with the machines, the most common of which was simply called
Gorton.  This is a digitalization of the Gorton font family.


## Variants in the Family
The Gorton typeface was available in several fonts of varying sizes and widths,
and in an inclined style.  Currently, I only have the normal width available.


## Creating the Output Fonts from the Template

Gorton was used for engraving, so, naturally, it features strokes of a constant
width for easier machining.  Different weights could be provided by simply
using a different size cutter.  Naturally, therefore, instead of trying to trace
each different weight, I have produced template splines matching the original
curves.  The template is then stroked to produce a font of the desired weight.

FontForge, helpfully, provides an expand stroke function which works fairly
well.  It's not perfect, but careful design of the template splines can work
around most issues.

I use a script to automatically stroke the glyphs and generate output font
files.  It uses the following widths for strokes:
* height/12 for light
* height/9 for normal
* height/8 for medium
* height/6 for bold/heavy

To use the stroking script, run the generateStrokes.ff script through FontForge,
e.g.: ```fontforge generateStrokes.ff gortondigital.sdf``` If you want to
execute the script using the File > Execute Script dialog, remove the top two
lines of the script, as you don't need to open an already open font file.
You'll also need to alter the ```Generate(``` call to give the right file name.


## Digitization Process
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
### Punctuation Marks
* ! Based approximately on the exclamation mark from the inclined style.
* " ' The ASCII straight quotes are somewhat based on the typographic quotes, but
are altered to be . . . straight.  If you want typographic quotes, they are
provided at the Win-1252 codepoint.
* \` This is just like the straight quotes, but rotated slightly.
* \# % + * / \ ^ @ I had no template to base these standard ASCII punctuation marks
on, but I still wanted them to be present, so I've provided my best guess at
designs for these glyphs that matches the original style of the typeface.
* \# This is inclined ever so slightly.
* $ This is primarily based on the S glyph.  The straight stroke is inclined
slightly.
* % This is based somewhat on the fractions, with the zero copied from the
underlined O (as in Nº).
* & This was traced from the ampersands found in the copy catalog.  The
resolution in those photos wasn't as good, so the glyph could probably be
improved.
* \* The asterisk has five points, because I like the five-point form.
* ( ) [ ] { } < > I had no source material for brackets, so I just took a guess.
The parentheses are based on an arc of a circle, with the width and height
matching the the square and curly brackets.
* \+ This is based on the minus provided.  The verticle stroke is the same length
as the horizontal stroke.
* \- , . : ; Based on provided high-resolution images.  The comma's curve could
possibly be improved, but since it gets stroked to the final form, it's a bit
hard to get exact.
* / \ I had no source material for slashes, so I guessed.
* = Also guessed, with width based on the minus.
* ? Based on the question mark provided in the inclined style, after using
Photoshop (the name-brand, not generic) to unskew it.  The resolution wasn't
great, so unskewing it gave suboptimal results---plus engraving machines don't
have optical skewing---so it's not an exact trace; I used my judgement to try to
get an authentic look.
* @ Based on the lower-case a, with a large circle around it.  What more could I
do?
* | The verticle bar is a guess.
* ~ NO TILDE is provided.  I might get around to inventing one, or I might not. TODO
* € Not provided, but it's on the TODO list.
* ‚ „ … Just copied from the comma and period codepoints.
* ‘ ’ “ ” Typographic quotes were provided in the original type copy.  They're
the same as the comma, just translated and rotated as needed.
* • · The middle dot is the same as the period, but raised to the middle.  The
bullet is bigger than the middle dot, by an amount that's a complete guess.
* – — The en- and em-dashes the exact same width as the N and M glyphs.
* ¢ The cent symbol is based on the lowercase c, and it doesn't work very well.
I should revise it. TODO
* £ The pound symbol is a total guess.
* ¥ Provided because it was easy to invent.
* ¦ A broken bar is provided, because why not?
* ° The degree symbol is just guess.  It's a cirle, what more could there be?
* ± I had something to base this on, but the positioning is a guess, because it
wasn't provided near other glyphs to judge height on.
* µ A mu is provided because it is useful for engraving metric units.  It is
based on the lowercase u, with the down stroke based on the descenders of p and
q, and the curl based on a.
* º × I had source material for this, so it's provided. 
* ÷ If multiplication is provided, then division should be, too, right?  It
wasn't, so this is just a guess.

### Numerals
* 0 Identical to capital O
* 1 Identical to capital I and lowercase l.  I'd like to provide an optional
variant with a serif in the future.
* 2 3 5 6 8 9 These were more traced than measured, though 6 and 9 are just
rotated copies.
* 4 Easily measured.
* 7 Also measured.  The arc was actually pretty easy.

### Uppercase Glyphs
Most of these weren't too hard.  It looked like the open curves (as in C and
S) had short straight sections at the end, so those are duplicated here.
* C It wasn't perfectly symmetric in my source material, so it isn't here,
either.
* G This was a bit hard to get right, but it matches pretty well now.
* K The lower leg seemed a bit longer, which is duplicated here.
* Q The stroke through the oval was more complicated than I expected.  It's a
fairly close match now.
* S The curve on this is based on arcs from ovals.  I'm not sure if that's
very accurate, but it seems to work.
* W This wasn't perfectly symmetric, oddly enough.  I wasn't sure if the slight
skew was due to how I straightened the image, or if it was intentional.  I
decided to make the angles fully symmetric, specifically 22/78°.

### Lowercase Glyphs
I didn't have high-resolution source material for these glyphs, so all of them
could be significantly improved.  The heights aren't uniform, and due to
low-resolution source material, I'm not sure if that's accurate or not.
* a Traced.  I did my best.
* b d p q Basically, these are just rotated/flipped variants of each other.
* c It's not exactly scaled down from the capital C.
* h Based on b, but straight.
* e Not an exact match to lowercase c.
* g This is kind of awful.  It can definitely be improved.
* s This isn't a scaled-down capital S; I traced it.  It could probably be
improved.
* u Like h, but mirroed and less a/descendy.
* y There a curl on this, but it could probably be improved.
