# Text File Compression using Huffman Algorithm

This program demonstrates text file compression using the Huffman coding algorithm implemented in C++. Huffman coding is a widely used technique for lossless data compression.

## How It Works

The program consists of several key components:

1. **Character Frequency Calculation**: 
   - Reads a text file to determine the frequency of each character present.
   - Characters with non-zero frequency are considered for compression.

2. **Huffman Tree Construction**: 
   - Constructs a Huffman tree using a priority queue (min-heap).
   - Huffman codes (bit sequences) are generated based on the tree structure.
   - Each character is assigned a unique Huffman code based on its frequency.

3. **Compression Process**: 
   - Converts each character in the input file into its corresponding Huffman code.
   - Writes these codes bit-by-bit into an output binary file.

4. **Compression Ratio Calculation**: 
   - Calculates the compression ratio achieved.
   - The compression ratio is the ratio of the original file size to the compressed file size.

5. **Output**: 
   - Generates a compressed file with a `.cmp` extension.
   - Outputs a file `codes.txt` containing the mapping of characters to their Huffman codes.

## Steps to Run

To run the program:

1. **Compile**: Compile the `compress.cpp` file using a C++ compiler.
   ```bash
   g++ compress.cpp -o compress

2.. **Execute**: Run the compiled executable (`compress.exe` on Windows or `./compress` on Linux).

3. **Input**: Enter the name of the text file you want to compress.

4. **Output**:
   - A compressed file with a `.cmp` extension will be generated.
   - The compression ratio achieved will be displayed.
   - The Huffman codes for each character will be stored in `codes.txt`.

## Example

Suppose you have a file named `input.txt` containing text to be compressed:

- **Input**: `input.txt`
- **Output**: `input.cmp` (compressed file)

After compression, you'll have:

- `codes.txt`: A file mapping characters to their Huffman codes.
- Display of compression ratio achieved.

## Notes

- The program uses Huffman coding to create variable-length codes for characters based on their frequency of occurrence.
- The `BitwiseWrite` class handles bit-wise writing to efficiently pack bits into bytes for the output file.
- Ensure the input file exists in the same directory or provide the full path when prompted.





# Text File Decompression using Huffman Algorithm

This program decompresses a text file that has been compressed using Huffman coding. Huffman coding is a technique for lossless data compression.

## How It Works

The program includes the following components:

1. **BitwiseRead Class**:
   - Reads bits from a binary compressed file to decode Huffman-encoded data.

2. **Huffman Class**:
   - Constructs a Huffman decoding tree based on the Huffman codes provided.
   - Decodes the compressed binary file using the Huffman decoding tree.

3. **Decompression Process**:
   - Reads the Huffman codes and builds the decoding tree.
   - Decodes the compressed binary file to recreate the original text.

4. **Output**:
   - Outputs the decompressed text to a file named `Decompressed.txt`.
   - Displays the total number of times the Huffman decoding tree was traversed.

## Steps to Run

To run the program:

1. **Compile**: Compile the `decompress.cpp` file using a C++ compiler.
   ```bash
   g++ decompress.cpp -o decompress



2. **Execute**: Run the compiled executable (`decompress.exe` on Windows or `./decompress` on Linux).

3. **Input**:
   - Enter the name of the Huffman codes file (e.g., `codes.txt`) when prompted.
   - Enter the name of the compressed file (with a `.cmp` extension) when prompted.

4. **Output**:
   - The decompressed text will be saved to `Decompressed.txt`.
   - The total number of tree traversals during decompression will be displayed.

## Example

Suppose you have a compressed file named `input.cmp` and the corresponding Huffman codes in `codes.txt`:

- **Huffman Codes File**: `codes.txt`
- **Compressed File**: `input.cmp`

After decompression, the program will create:

- `Decompressed.txt`: The decompressed original text.

## Notes

- The program uses Huffman coding to decode the binary data efficiently.
- Ensure the Huffman codes file (`codes.txt`) and the compressed file (`input.cmp`) are in the same directory or provide the full path when prompted.

This program allows you to decompress files compressed using Huffman coding, demonstrating the process of decoding and restoring original text from compressed binary data in a practical C++ implementation.
