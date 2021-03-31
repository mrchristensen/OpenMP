# OpenMP

Your task is to parallelize the computation of the Mandelbrot set code found at https://gist.github.com/andrejbauer/7919569

First, you will need to learn a bit about the Mandelbrot set. Look at the Wikipedia entry for the Mandelbrot set. You can find it at https://en.wikipedia.org/wiki/Mandelbrot_set

Then download the code from GitHub and get it working sequentially.

This code consists of one major loop nest that can be parallelized, but it has a problem. Every iteration is writing into the file, and it must be written in order. You will need to save all the entries somehow and then write them all out after the computation. I strongly suggest you get this working before you parallelize the code.

After getting the file issues solved, parallelize the code using OpenMP directives.

NOTE: You may not use the "-O" (optimize) flag when compiling your code with gcc.  Unfortunately, that would take care of some of the work for you!

## Submission:
You will submit your working code in the file mandelbrot.c.

1. In a comment at the top of your code, report a) the number of (virtual) cores on your machine:

cat /proc/cpuinfo  | grep ^processor | wc -l

and b) your compute times (not file writing) for 1, 2, 4, and 8 threads using the following command line (i.e., not the ones in the file!):

./mandelbrot 0.27085 0.27100 0.004640 0.004810 1000 8192 pic.ppm

2. Upload mandelbrot.c to the assignment page on LearningSuite.

## Grading:

10 points - code compiles and works properly

10 points - for compute times