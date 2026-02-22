# CSV Data Cleaner

## Overview
A Python utility that cleans messy CSV files by:

- Removing invalid rows
- Validating numeric columns
- Trimming whitespace
- Standardizing capitalization
- Skipping rows with missing or incorrect numeric data

## Example Input

name,age,city,score  
 alice , 19 , hyd , 72  
BOB, , mumbai, 55  
charlie, 21, , 88  
david, twenty, delhi, 91  

## Example Output

name,age,city,score  
Alice,19,Hyd,72  
Charlie,21,,88  

## How It Works

- Uses `csv.DictReader` to read structured data
- Applies string cleaning methods (`strip()`, `capitalize()`)
- Validates numeric columns using `try/except`
- Writes cleaned results using `csv.writer`

## How To Run

```bash
python cleaner.py
