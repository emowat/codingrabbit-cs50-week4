## Problem to Solve

Perhaps the simplest way to represent an image is with a grid of pixels (dots), each of which can be of a different color. For black-and-white images, we thus need 1 bit per pixel. But for color images, we need more bits! In a 24-bit BMP (Bitmap) image, each pixel is represented by 3 bytes (24 bits) - one byte each for the amount of Red, Green, and Blue (RGB) in the pixel.

By manipulating these RGB values, we can apply photo filters! 
*   **Grayscale**: A pixel takes on a shade of gray when its red, green, and blue values are all equal.
*   **Sepia**: Takes the original RGB values and applies an algorithm to compute new RGB values to give the image an old-timey reddish-brown feel.
*   **Reflection**: Swaps pixels on the left side of the image with pixels on the right side.
*   **Blur**: Sets each pixel to the average color of all its neighboring pixels.

In a file called `helpers.c` in a folder called `filter-less`, create a program to apply these filters to BMP images.

*For the full background on BMP files, RGB values, and a detailed walkthrough, read the official instructions here: [CS50 Filter (Less) Instructions](https://cs50.harvard.edu/x/psets/4/filter/less/)*

## How to Begin

You need to download the "distribution code" which contains the scaffolding for the `filter` program and some sample BMP images. 

Open the terminal window at the bottom of your screen. Ensure your terminal is in the main workspace directory (it should look like `student@codespace:/workspaces/codingrabbit-cs50-week4$`). 

Run the following commands one by one to download the ZIP file, extract it, and clean up the ZIP:

```bash
curl -O https://cdn.cs50.net/2026/x/psets/4/filter-less.zip
unzip filter-less.zip
rm filter-less.zip
```

Extracting the ZIP will automatically populate this `filter-less` folder with the starter code and an `images/` directory. Now, change your terminal directory into this folder:

```bash
cd filter-less
```

You can now use the `code` command to open the `helpers.c` file in the editor:

```bash
code helpers.c
```

## Instructions

The distribution code already handles all the complicated file I/O for reading and writing the BMP headers. All you need to do is implement the filter logic in `helpers.c`! 

Complete the four functions in `helpers.c`:
1.  **`grayscale`**: Calculate the average of the red, green, and blue values for each pixel, and set all three to that average.
2.  **`sepia`**: Apply the sepia formula to calculate new RGB values. Ensure you cap the maximum value at 255!
3.  **`reflect`**: Horizontally mirror the image by swapping pixels on the left side of a row with the right side.
4.  **`blur`**: Calculate the average color of a pixel's surrounding 3x3 grid (being careful of the edges!). 

## How to Test

Recall that you can compile your program by running:

```bash
make filter
```

If it compiles successfully, run your program with the `-g` flag (for Grayscale) on the `yard.bmp` image:

```bash
./filter -g images/yard.bmp out.bmp
```

You can then view the new `out.bmp` file by double-clicking it in the file explorer! Test the other flags too: `-s` for sepia, `-r` for reflect, and `-b` for blur.

If you get stuck, remember to **click the Coding Rabbit icon** on the left sidebar to ask your AI Teaching Assistant for hints!
