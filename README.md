# Mandelbrot
Mandelbrot set generator in Dyalog APL

To reduce the number of pixels that need to be calculated, this code uses Boundary Tracing.

All "boundries" within the Mandelbrot Set are continous, and never cross.

All boundries pass between two adjecent pixels, never on them. Several boundries may pass between the same two pixels. 

The code tries only to calculate the pixels that lie next to boundries within the selected area.

Pixels which do not lie adjecent to boundary can then be "flood filled" with the same value as the pixel adjecent to the boundary. 

Currently, the algorithem used to Flood Fill the space (in the "black hole" areas) sometimes fails, and a coloured horizental line is produced.
I am working still working on fixing this bug.

The Bitmap is created using CMap and CBits. The animation is produced by rotating the values in CMap in a cycle.
