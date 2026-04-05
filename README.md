# ImageManipulator

A C# desktop application to encrypt, decrypt, compress, and decompress images — with a simple form-based GUI to perform and visualize operations.

## Features

- **Encryption** — encrypts images using the Linear Feedback Shift Register (LFSR) algorithm
- **Decryption** — reverses the encryption to restore the original image
- **Compression** — compresses images using Huffman encoding
- **Decompression** — restores compressed images by reversing the Huffman encoding
- **Benchmarking** — evaluates and reports the compression ratio

## How It Works

The app exposes three main classes:

`ImageOperations` handles common image I/O — opening, saving, and reading dimensions. `Compression` contains the Huffman-based `CompressImage()` and `DecompressImage()` logic. `Encryption` contains the LFSR-based `EncryptImage()` and `DecryptImage()` logic.

A custom `PriorityQueue` is also included to support the Huffman tree construction.

## Project Structure

```
├── ImageEncryptCompress/       # Main C# project source
├── PriorityQueue               # Priority queue implementation
├── SampleCases_Compression/    # Sample images for compression testing
├── SampleCases_Encryption/     # Sample images for encryption testing
├── results/                    # Output results
├── design_doc.md               # Design document
├── ImageEncryptCompression.sln # Visual Studio solution file
└── README.md
```

## Getting Started

### Prerequisites

- .NET SDK
- Visual Studio (recommended)

### Run

Open `ImageEncryptCompression.sln` in Visual Studio, build the solution, and run. Use the GUI to load an image and choose an operation.

## License

MIT — see [LICENSE.txt](LICENSE.txt) for details.
