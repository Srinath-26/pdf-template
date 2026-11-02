# PDF Notebook Template

A simple Python project that creates a lined PDF notebook from a CSV file. Each topic gets a heading on its first page, a topic footer on every page, and a chosen number of pages for notes.

## Features

- A4 pages in portrait orientation
- Horizontal lines for handwritten notes
- Topic headings and footers
- Customizable topics and page counts

## Setup

You need Python 3 installed. From the project folder, install the required libraries:

```bash
python3 -m pip install fpdf==1.7.2 pandas
```

## Usage

1. Edit `topics.csv` to choose your topics and page counts. For example:

   ```csv
   Order,Topic,Pages
   1,Variables,2
   2,Lists,3
   3,Functions,3    
   ```

   `Topic` is the heading and footer text. `Pages` is the total number of pages for that topic; use a positive whole number. Topics appear in CSV row order—the script does not use the `Order` column to sort them.

2. Run the script from the project folder:

   ```bash
   python3 main.py
   ```

3. Open `output.pdf` to view or print your notebook. Running the script again replaces this file.

## Project Files

- `main.py` — Generates the PDF using FPDF and pandas.
- `topics.csv` — Stores topic names and page counts.
- `output.pdf` — The generated notebook.
