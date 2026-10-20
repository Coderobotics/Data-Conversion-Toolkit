# Data Conversion Toolkit

Data Conversion Toolkit is a self-hosted Python and Django web application with 8 utilities for converting tabular data between CSV, Excel, JSON, JSONL, and Parquet formats. All conversions run locally in the browser with no data sent to external services, making it suitable for privacy-sensitive workflows. It includes user accounts, conversion history, and a test CSV generator, and is built on pyarrow, pandas, openpyxl, and Faker.

<img src="https://www.coderobotics.com/frontend/assets/icon/data-conversion-toolkit-python-django-script.jpg">

Stop uploading sensitive data to online converters just to change its format. Data Conversion Toolkit is a self-hosted, browser-based Django app that converts between CSV, Excel, JSON, JSONL, and Parquet entirely on your own machine — with per-user accounts and a history of past conversions. Each utility is independent, easy to understand, and ready to use straight from the browser.

What You Get
 
CSV => Parquet — stream a CSV file into Parquet, inferring the schema from the data itself.
Parquet => CSV — read Parquet in row-group batches and stream it back out as CSV.
Excel => Parquet — convert an .xlsx worksheet to Parquet without loading the whole workbook into memory (row-by-row streaming read), with an optional sheet name.
Parquet => Excel — export Parquet to an .xlsx workbook, automatically splitting into multiple sheets if the row count exceeds Excel's per-sheet limit.
JSON => Parquet — convert a JSON array of objects, including nested objects/arrays, to Parquet.
Parquet => JSON — convert Parquet back to a standard JSON array, preserving nested structures.
JSONL => Parquet — stream newline-delimited JSON into Parquet.
Generate Test CSV — create a realistic random dataset with configurable columns (name:type pairs), row count, and an optional random seed for reproducibility. Supported types: int, float, name, email, date, bool, address, word, uuid.
Plus, built into the app:

Accounts — sign up / log in with Django auth; every tool requires login.
History — every conversion is logged with status and a re-download link, scoped to your own account (other users can't access your files, even by guessing a download URL).
Delete — remove a result and its file right after generating it or later from History, with a confirmation prompt before it's gone for good.
Atomic output writes — every conversion writes to a temporary .part file and renames it into place only on success, so a crash mid-conversion never leaves a corrupt file behind.
Why This Toolkit?
 
Many data conversion services require uploading files to an external website — not acceptable when working with company data, customer datasets, financial information, or files covered by internal security policies.

These utilities run entirely on your own machine. Input files are processed locally and are never sent to an external conversion service or API.

They're also useful any time you just need a small, reliable conversion tool instead of standing up a full web application.

No web server dependency
No API keys required
No external conversion service required
Perfect For
 
Python developers & backend engineers
Data engineers and ETL pipeline builders
Data analysts and QA engineers
Local data processing & test data generation
Batch data conversion
Projects with strict data privacy requirements
Anyone who needs simple, reliable CLI-style conversion utilities without the CLI

Tech Stack
 
Python 3 + Django
pyarrow — CSV/JSON/JSONL => Parquet, streaming reads/writes
pandas — batch-to-CSV conversion
openpyxl — Excel read (streaming) and write, including multi-sheet export
Faker — realistic test data generation
Bootstrap 5 (CDN) UI with custom theming and Google Fonts (Space Grotesk, IBM Plex Sans, JetBrains Mono)
SQLite (default Django dev database)

Prerequisites
 
Python 3.10+ installed and on your PATH
Git (optional, only for version control)

More details and Download link:
https://www.coderobotics.com/product/data-conversion-toolkit
