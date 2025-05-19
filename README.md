## OpenSource - Assignment 2
This repository contains three Bash scripts designed to preprocess, clean, and analyze a CSV dataset related to electricity production from different sources (e.g., solar/wind and coal). These scripts are developed as part of a data processing assignment.



#### **Scripts Overview**

##### 1. empty_cells

- *Purpose: Detects and reports rows in a file that contain empty fields.*
- *Input: A tab-separated value file (typically the output from preprocess)*
- *Output: Prints line numbers and content with empty fields to stderr and exits with status code 1 if any are found.*

*Usage:*

```bash
./empty_cells <input_file>
```

------



##### 2. preprocess

- *Purpose: Cleans and reformats a raw dataset by:*
  - *Converting separators (e.g., ; to tabs)*
  - *Removing empty lines*
  - *Normalizing line endings*
- *Input: A raw .csv or .txt file with ;-separated values*
- *Output: A cleaned version of the file in tab-separated format*

*Usage:*

```bash
./preprocess <input_file> [separator]
```

- If no separator is provided, defaults to ;.

------



##### 3. analysis

- *Function: Performs statistical analysis on a board game dataset (TSV format).*
- *Input: A tab-separated file (.tsv) with 14 columns.*
- *Output:*
  - *Most common game mechanic*
  - *Most common game domain/theme*
  - *Two Pearson correlation coefficients:*
    - *Year of publication vs. average rating*
    - *Game complexity vs. average rating*

*Usage:*

```bash
./analysis <input_file.tsv>
```

------



#### **Requirements**

- GNU awk
- sed
- Standard Unix command-line tools (e.g., sort, cut, grep)

Ensure all scripts have execute permissions:

```bash
chmod +x preprocess empty_cells analysis
```

------



#### **Notes**

- The preprocess script ensures the dataset is in a standardized format for further processing.
- empty_cells should be run before analysis to verify data completeness.
- Error messages and invalid input formats are reported to stderr.

------



#### **Author**

Ryan Chang

Student ID: 23691038

University of Western Australia

