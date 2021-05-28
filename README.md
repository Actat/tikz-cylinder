# tikz-cylinder

## Usage

You can compile `cylinder.tex` and get `cylinder.pdf`.

```
$ latex cylinder.tex
$ dvipdfmx cylinder.dvi
```

If you want to use in your project, you can follow the three steps below.
1. Copy paste the `\newcommand` part in cylinder.tex to your file.
1. In `tkzpicture`, set rotated coordinates by `\tdplotsetrotatedcoords{&alpha;}{&beta;}{&gamma;}`.
1. Call `\tdcylinder` to draw cylinder in the rotated coordinates.

`\tdcylinder` takes 7 parameters.

Syntax: \tdcylinder{x}{y}{z}{r}{h}{&theta;}{&phi;};

|Parameter|Description|
|:-:|:--|
|x|The x-compornent of the position vector of center of bottom circle in the rortated coordinate frame.|
|y|The y-compornent of the position vector of center of bottom circle in the rortated coordinate frame.|
|z|The z-compornent of the position vector of center of bottom circle in the rortated coordinate frame.|
|r|The radius of the cylinder.|
|h|The height of the cylinder.|
|&theta;|The angle (in degrees) through which the coordinate frame is rotated about the x axis. The value set in `\tdplotsetmaincoords`.|
|&phi;|The angle (in degrees) through which the coordinate frame is rotated about the z axis. The value set in `\tdplotsetmaincoords`.|

## Known issues

1. Cause error when &theta; of the main coordinate system is set to 0.
1. When viewing a cylinder from the bottom, the `\filldraw` commands must be done in reverse order.
