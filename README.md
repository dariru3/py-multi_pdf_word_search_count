# Multi-PDF Word Count

This Python script scans through multiple PDF files and counts the occurrences of a list of specified words. The results are then written to a summary CSV file. 

## Requirements

- Python 3
- PyMuPDF (`fitz`)
- csv

## Configuration

The script reads from a configuration file `config.py` which should contain a list of PDF files and a CSV file. The CSV file contains the list of words to be searched.

Example `config.py`:

```python
config = {
    "source files": ["file1.pdf", "file2.pdf", ...],
    "keywords list": "keywords.csv"
}
```

Example `keywords.csv`:

```
_, _, _, word1
_, _, _, word2
_, _, _, word3
```

The search terms are in the fourth column of the CSV file.

## Running the Script

To run the script, use the command:

```
python main.py
```

Replace `main.py` with the filename of your script if it's different.

The script will output a CSV file named `summary.csv` with the count of each word in each PDF file. The CSV file will have one row for each search term in each input file, with the fields 'Input file', 'Search Term', and 'Matching Instances'.

## Note

This script is designed to handle Japanese text. Make sure your files are UTF-8 encoded to ensure the Japanese characters are read correctly.
