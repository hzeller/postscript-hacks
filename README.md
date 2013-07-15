Little useful PostScript hacks
------------------------------

PostScript is a programming language that allows to define highly precise, real
coordinate graphics, which I often use to directly print out geometric
accurate pieces. This is a collection of hacks that might be worthwhile
for others to use. Consider them (c) H.Zeller <h.zeller@acm.org>,
licensed Creative Commons BY-SA.

All of these typically have a configuration section at the top that allows
to modify the parameters. Just configure, verify in ghostscript and print
out. If your printer is properly calibrated, it should print this in the
exact measurements (beware certain PostScript -> PDF conversion with subsequent
PDF printing: these programs often attempt to be too smart for their own good
and scale the image to what they think the margins of the paper is).


### Encoder wheel
For rotational applications, it is often needed to keep track of the
turns. The `encoder-wheel.ps` is freely configurable in radius and number
of segments displayed.

![Image or encoder wheel][wheel-img]

### SMD ruler
If you're soldering a lot of SMD parts and need to check measurements or
count leads, the `smd-ruler.ps` might be useful for you.

![Image of ruler][ruler-img]

[wheel-img]: https://github.com/hzeller/postscript-hacks/raw/master/img/wheel-picture.png
[ruler-img]: https://github.com/hzeller/postscript-hacks/raw/master/img/smd-ruler.jpg
