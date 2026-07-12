## Problem to Solve

WAV files are a common file format for storing audio. In this problem, you'll write a program to modify the volume of an audio file! 

A WAV file consists of a "header" (which contains metadata like the sampling rate and audio format) followed by a sequence of "samples" (the actual audio data). For the files we'll be working with, the header is exactly 44 bytes long, and each audio sample is a 2-byte (16-bit) integer representing the audio signal at a specific point in time.

To scale the volume of the audio by a given factor, you simply need to multiply each 2-byte audio sample by that factor! 

In a file called `volume.c` in a folder called `volume`, create a program to scale the volume of a WAV file.

*For the full background on WAV files, audio samples, and a detailed walkthrough, read the official instructions here: [CS50 Volume Instructions](https://cs50.harvard.edu/x/psets/4/volume/)*

## How to Begin

You need to download the "distribution code" which contains the scaffolding for the `volume` program and some sample WAV files. 

Open the terminal window at the bottom of your screen. Ensure your terminal is in the main workspace directory (it should look like `student@codespace:/workspaces/codingrabbit-cs50-week4$`). 

Run the following commands one by one to download the ZIP file, extract it, and clean up the ZIP:

```bash
curl -O https://cdn.cs50.net/2026/x/psets/4/volume.zip
unzip volume.zip
rm volume.zip
```

Extracting the ZIP will automatically populate this `volume` folder with the `volume.c` starter code and an `input.wav` file. Now, change your terminal directory into this folder:

```bash
cd volume
```

You can now use the `code` command to open the file in the editor:

```bash
code volume.c
```

## Instructions

The distribution code provides the `main` function which handles opening the input and output files and parsing the command line arguments. Your job is to complete the two TODOs:

1.  **Copy the Header**: Read exactly 44 bytes from the input file and write them directly to the output file. (Hint: use an array of `uint8_t` for this).
2.  **Scale the Samples**: Read the rest of the data from the input file, one 2-byte sample at a time. Multiply each sample by the `factor`, and write the new sample to the output file. (Hint: use a `int16_t` for this, and loop until you reach the end of the file using `fread`).

## How to Test

Recall that you can compile your program by running:

```bash
make volume
```

If it compiles successfully, run your program to double the volume:

```bash
./volume input.wav output.wav 2.0
```

You can then listen to the new `output.wav` file by double-clicking it in the file explorer!

If you see an error message or get stuck trying to use `fread` and `fwrite`, remember to **click the Coding Rabbit icon** on the left sidebar to ask your AI Teaching Assistant for hints!
