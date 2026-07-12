## Problem to Solve

In anticipation of this problem, we spent the past several days taking photos around campus, all of which were saved on a digital camera as JPEGs on a memory card. Unfortunately, we somehow deleted them all! Thankfully, in the computer world, "deleted" tends not to mean "deleted" so much as "forgotten." Even though the camera insists that the card is now blank, we're pretty sure that's not quite true.

Your task is to write a program that recovers these deleted JPEGs from a forensic image of the memory card. 

JPEG files always start with a distinct "signature": the first three bytes are `0xff`, `0xd8`, and `0xff`, and the fourth byte's first four bits are `1110` (meaning the fourth byte is somewhere between `0xe0` and `0xef`). Furthermore, digital cameras often write to memory cards in blocks of 512 bytes. Therefore, each JPEG file will begin exactly at the start of a 512-byte block.

In a file called `recover.c` in a folder called `recover`, write a program to recover JPEGs from a memory card.

*For the full background on memory forensics and a detailed walkthrough, read the official instructions here: [CS50 Recover Instructions](https://cs50.harvard.edu/x/psets/4/recover/)*

## How to Begin

You need to download the "distribution code" which contains the raw forensic image of the memory card (`card.raw`).

Open the terminal window at the bottom of your screen. Ensure your terminal is in the main workspace directory (it should look like `student@codespace:/workspaces/codingrabbit-cs50-week4$`). 

Run the following commands one by one to download the ZIP file, extract it, and clean up the ZIP:

```bash
curl -O https://cdn.cs50.net/2026/x/psets/4/recover.zip
unzip recover.zip
rm recover.zip
```

Extracting the ZIP will automatically populate this `recover` folder with the starter code and the `card.raw` file. Now, change your terminal directory into this folder:

```bash
cd recover
```

You can now use the `code` command to open the `recover.c` file in the editor:

```bash
code recover.c
```

## Instructions

Your program should accept exactly one command-line argument: the name of the forensic image from which to recover JPEGs (e.g. `card.raw`).

1.  **Open the memory card:** Use `fopen` to read `card.raw`.
2.  **Read the card:** Use a `while` loop with `fread` to read the memory card 512 bytes at a time.
3.  **Look for JPEGs:** In each 512-byte block, check the first 4 bytes to see if they match the JPEG signature.
    *   If you find a new JPEG signature, you've found a new file! You'll need to close the previous JPEG file (if one was already open) and open a new one. 
    *   The files should be named `000.jpg`, `001.jpg`, `002.jpg`, etc. (Hint: use `sprintf`).
4.  **Write to the file:** If you are currently in the middle of reading a JPEG, write the 512-byte block to your open output file using `fwrite`.

## How to Test

Recall that you can compile your program by running:

```bash
make recover
```

If it compiles successfully, run your program on the memory card:

```bash
./recover card.raw
```

If it works correctly, you should suddenly see fifty `.jpg` files appear in your folder! Click on them to see the recovered images!

If you see an error message, get a segmentation fault, or the images won't open, remember to **click the Coding Rabbit icon** on the left sidebar to ask your AI Teaching Assistant for hints!
