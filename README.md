# Mandelbrot
Mandelbrot set generator in Dyalog APL

To reduce the number of pixels that need to be calculated, this code uses Boundary Tracing.

All "boundaries" within the Mandelbrot Set are continuous, and never cross.

All boundaries pass between two adjacent pixels, never on them. Several boundaries may pass between the same two pixels. 

The code tries only to calculate the pixels that lie next to boundaries within the selected area.

Pixels which do not lie adjacent to boundary can then be "flood filled" with the same value as the pixel adjacent to the boundary. 

Currently, the algorithm used to Flood Fill the space (in the "black hole" areas) sometimes fails, and a coloured horizontal line is produced.
I am working still working on fixing this bug.

The Bitmap is created using CMap and CBits. The animation is produced by rotating the values in CMap in a cycle.

The auto start ⌷LX should be set to run the function "lx".
