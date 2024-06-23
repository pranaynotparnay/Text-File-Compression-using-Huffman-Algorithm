# Text-File-Compression-using-Huffman-Algorithm
# Text File Compression using Huffman Algorithm

This program compresses text files using the Huffman Algorithm. The compression process reduces the size of the text file by encoding characters with variable-length codes based on their frequencies.

## Features

- Compresses text files using Huffman coding.
- Generates a frequency table of characters in the text file.
- Creates Huffman codes for each character.
- Writes the compressed data to a new file with the `.cmp` extension.
- Calculates and displays the compression ratio.

## How It Works

### Compression

1. **Calculate Character Frequencies:** 
   - The program reads the input file and calculates the frequency of each character.
   - Characters with non-zero frequencies are stored in a character map.

2. **Build Huffman Tree:**
   - A min-heap is used to build the Huffman tree. Nodes with the lowest frequencies are combined to create parent nodes, forming the tree.

3. **Generate Huffman Codes:**
   - The program traverses the Huffman tree to generate codes for each character.
   - These codes are stored in the character map.

4. **Write Compressed Data:**
   - The Huffman codes are written bit by bit to the output file using a bitwise writer.
   - The program also generates a `codes.txt` file containing the character-to-code mappings.

5. **Calculate Compression Ratio:**
   - The program calculates and displays the compression ratio by comparing the original file size with the compressed file size.

## Results

The compressed file is saved with a `.cmp` extension, and the compression ratio is displayed at the end of the process.

## How to Run

### Prerequisites

- A C++ compiler (e.g., g++, clang++)
- The input text file to compress

### Steps

1. **Compile the Source Code:**

   ```sh
   g++ compress.cpp -o compress
