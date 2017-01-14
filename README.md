Little useful PostScript hacks
------------------------------

PostScript is a programming language that allows to define highly precise, real
coordinate graphics, which I often use to directly print out geometric
accurate pieces.

This is a random collection of hacks that might be worthwhile
for others to use. Consider them (c) H.Zeller <h.zeller@acm.org>,
licensed Creative Commons BY-SA.

All of these typically have a configuration section at the top that allows
to modify the parameters. Just configure, verify in ghostscript and print
out. If your printer is properly calibrated, it should print this in the
exact measurements (beware certain PostScript -> PDF conversion with subsequent
PDF printing: these programs often attempt to be too smart for their own good
and scale the image to what they think the margins of the paper is. So make sure
to always set the margins to zero).

### Encoder wheel
For rotational applications, it is often needed to keep track of the
turns. The [`encoder-wheel.ps`](./encoder-wheel.ps) is freely configurable in
radius and number of segments displayed.

Here configured for 12 steps with an inner radius of 20mm and an outer radius
of 30mm. The output also includes some helpful measurements:

![Image or encoder wheel][wheel-img]

### SMD ruler
If you're soldering a lot of SMD parts and need to check measurements or
count leads, the [`smd-ruler.ps`](./smd-ruler.ps) might be useful for you.

![Image of ruler][ruler-img]

### Metric/Imperial sizes
The [`metric-imperial-diameter.ps`](./metric-imperial-diameter.ps) creates
a chart to get a visual understanding about the relationship between metric
and imperial measurements and hole-sizes. Typically good to gauge drill sizes.

### Page Label
Just given a simple list of labels, create full-page labels that fit into
a rectangular space best, using the largest font-size possible. This is the
[`page-label.ps`](./page-label.ps) script.

Just append at the end of the PostScript page. For instance

```
%%Page:
(Goggles\nGloves) show-max

%%Page:
(Drills\nMills) show-max
```

.. creates these

![Page-labels][page-label]

### Box label
The [`box-label.ps`](./box-label.ps) script creates little labels for SMD boxes.
To be printed on blank sticker page. With a simple script addition appended
at the bottom like this:

```
{ (1.0) Ohm } box
{ (1.1) Ohm } box
{ (1.2) Ohm } box
% and so on
```

... the output is like:

![Box Label][box-label-img]

[box-label-img]: ./img/box-label.png
[wheel-img]: ./img/wheel-picture.png
[ruler-img]: ./img/smd-ruler.jpg
[page-label]: ./img/page-label.png
