# Comparative-Analysis-of-Lossless-Decompression-Techniques-On-Genetic-Code-for-Biological-Species

## Motivation

In every mRNA sequence, there’s approximately 3 million nucleotides (A, U, G, C). To store these as strings of lengths greater than 3 million is tedious and would take up a lot of storage.
Compression of genomic sequences can decrease the storage requirements, and increase the transmission speed which can be useful for synthesis of medicines and genetic engineering. Various lossless data compression algorithms may be used to achieve this.
This project serves the purpose of compressing the given strings using Huffman Encoding, Run Length Encoding and LZW compression, while simultaneously acting as a tool to compare the compression algorithms and calculate the save percentage.

## Algorithmic Strategy

RLE, LZW and Huffman Coding are all lossless data compression algorithms that can be used to encode as well as decode our input of the rna sequence. Reasons for choosing these algorithms:
#### RLE: 
Counts the consecutive repetition amount of a symbol and uses that value to represent the run.
Efficient with files that contain lots of repetitive data and does not require much CPU horsepower.
#### LZW: 
Creates a key value pair for every new sequence of input
The key value dictionary does not need to be passed on to the decompression part 
#### Huffman Coding: 
Huffman takes advantage of the disparity between frequencies and uses less storage for the frequently occurring characters
This is at the expense of using more storage for rare characters, however as are inputs would be only 4 characters, this drawback does not apply here

## Software/Tools Requirements

### Software Requirements
Tkinter
Python 3
Jupyter Notebook
OS - Windows/Linux/macOS

## Modules

- Tkinter module for GUI (buttons, window,etc)
- RLE Compression + Decompression
- LZW Compression + Decompression 
- Huffman Encoding + Decoding

## Results
For every compression algorithm, the size of the data is calculated before and after compression, and then the save percentage is calculated
In most cases, it appears that Huffman Coding has the highest save percentage
For large strings, LZW requires a bigger dictionary size and in general, for larger file sizes, LZW needs better computing resources or an overflow problem is observed
Generally, the only drawback of Huffman is that based on the rarity of certain characters the depth of the tree is increased and the binary code word will be large in length. However, this does not apply to our input as they are a combination of only four letters
RLE is not optimal as in some cases, the encoded data is larger in size than the original. This occurs when the letters have a low continuous frequency. However, if our input has many continuous characters, in some cases, RLE is better than Huffman.   

