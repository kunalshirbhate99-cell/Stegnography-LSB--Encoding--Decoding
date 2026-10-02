# Steganography – LSB Encoding & Decoding

## Project Overview

A C-based Steganography project that implements the Least Significant Bit (LSB) technique to hide secret data inside BMP images. It allows users to encode secret messages or files into an image and retrieve the hidden data through decoding.

## Features

* Encode secret files into BMP images using LSB technique.
* Decode and retrieve hidden data from stego images.
* Verify encoded data using a Magic String.
* Check image capacity before encoding.
* Support for secret file size and extension encoding.
* Preserve the original BMP image header.

## Technologies Used

* C Programming
* File Handling
* Pointers
* Structures
* Bitwise Operations
* Dynamic Memory Concepts
* LSB Steganography

## Project Structure

```text
Steganography/
├── main.c
├── encode.c
├── encode.h
├── decode.c
├── decode.h
├── common.h
├── types.h
└── README.md
```

## How It Works

### Encoding

1. Read and validate command-line arguments.
2. Open the source BMP image and secret file.
3. Check whether the image has sufficient capacity.
4. Copy the BMP header into the output image.
5. Encode the Magic String, secret file extension, file size, and secret file data into the image using LSB.
6. Generate the stego image containing the hidden data.

### Decoding

1. Open the stego image.
2. Read and verify the Magic String.
3. Decode the secret file extension and file size.
4. Extract the hidden data using LSB.
5. Reconstruct and save the original secret file.

## Compilation

Compile the source files using GCC:

```bash
gcc main.c encode.c decode.c -o steganography
```

## Execution

### Encoding

```bash
./steganography -e beautiful.bmp secret.txt
```

### Decoding

```bash
./steganography -d stego_img.bmp
```

**Note:** Command-line options and filenames should match the implementation.

## Learning Outcomes

* Understanding file handling in C.
* Working with BMP image files.
* Applying bitwise operators for LSB manipulation.
* Implementing encoding and decoding algorithms.
* Understanding pointers, structures, and command-line arguments.
* Handling binary data and file operations.

## Author

**Kunal Shirbhate**
