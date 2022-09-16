# Batch File Packer - A batch file packer/compressor

Batch File Packer is a small utility that allows you to pack any file into a self-extracting batch script. The overhead is very small (~250 bytes) and uses base64 encoding along with cabinet file compression (CAB). This is used to achieve maximum compression and a faster script decompression as the extracted file will be smaller.

# Usage

## File compression

Compress a file: `BFP <file>`
Compress a file with a custom output file: `BFP <file> -o <outfile>`

## Decompression
Decompress a file: `BFP -d <file>`

## Integrity check 

With BFP you can do an integrity check on the extracted file before running it in order to ensure that the decompression was successful.
Simply use `BFP -h<hashing> <file>`

Supported hash algorithms:

- SHA256
- SHA384
- SHA512
- SHA1
- MD2
- MD4
- MD5

## Maximum compression

7-Zip extracting
If 7-Zip is installed, you can use the `-7` switch to use 7-Zip instead of the regular CAB.
Usage: 
`BFP -7 <file>`



Usage:
`BFP -m <file>`

**WARNING: This should ONLY be used on batch files. This is a lossless compression**.

**Copyright (c) 2022 anic17 Software**
