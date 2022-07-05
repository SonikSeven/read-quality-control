# Read Quality Control

This project provides a Python script for analyzing DNA reads from gzip-compressed files. The primary functionality includes calculating various statistical properties of the DNA sequences, such as the average length of the reads, the percentage of undefined bases in the sequences, and the GC content average across all reads. 

## Features

- Reads DNA sequence data from gzip-compressed files
- Calculates average length of DNA sequences
- Identifies and counts repeated sequences
- Calculates the percentage of reads containing undefined bases ('N')
- Computes the average GC content across all sequences
- Identifies the file with the highest average GC content and displays the statistical analysis of the DNA sequences from that file

## Requirements

- [Python 3](https://www.python.org/downloads/)

## Installation

This application is written in Python, so you'll need Python installed on your computer to run it. If you don't have Python installed, you can download it from [python.org](https://www.python.org/downloads/).

To install this project, clone the repository to your local machine:

```
git clone https://github.com/SonikSeven/read-quality-control.git
```

## How to Run

To run the program, follow these steps:

1. Open a terminal and navigate to the directory where the script is located.
2. Run the script using Python:

```
python main.py
```

## Usage

1. **Prepare Your Data**: Your DNA sequence data should be stored in gzip-compressed files. Each DNA sequence should be in a new line. The script expects that every 4th line starting from the second line (`[1::4]`) in the gzip file contains the sequence data to be analyzed.

2. **Running the Script**: Run the script (see the [How to Run](#how-to-run) section above).

3. **Input**: When prompted, enter the path to each of your gzip-compressed DNA data files. You will need to input paths for three files one by one.

```plaintext
/path/to/your/firstfile.gz
/path/to/your/secondfile.gz
/path/to/your/thirdfile.gz
```

4. **Output**: The script will analyze the data from the three provided files and print out a summary of the file with the highest average GC content. The summary includes:
    - Total number of reads
    - Average sequence length
    - Number of repeating sequences
    - Number of reads with undefined bases ('N')
    - Average GC content percentage
    - Percentage of reads with undefined bases per sequence

## Example

After running the script and inputting the file paths, you may see output to the following:

```
Reads in the file = 1000
Reads sequence average length = 150

Repeats = 2
Reads with Ns = 10

GC content average = 47.25%
Ns per read sequence = 0.1%
```

This output provides a quick overview of the DNA sequences in the gzip file with the highest GC content, allowing researchers to assess the quality and characteristics of the sequences.

## License

This project is licensed under the [MIT License](LICENSE.txt).
