# Board Game Data Analysis

**Author**: Dulya Murage

GitHub repo : https://github.com/DulyaMur/Assignment2_24910402

## Overview

This project handles analyzing the dataset from **Board Game Geek** on Kaggle. The analysis is conducted using Shell scripts.  
The goal is to answer the following four research questions:

1. **What is the most popular domain and most popular game mechanic?**
2. **What is the correlation between a game's publication year and its average rating?**
3. **What is the correlation between a game's complexity and its average rating?**

## File Structure

```plaintext
project-directory/
│
├── analysis          # Top-level analysis script
├── preprocess        # Top-level preprocessing script
├── empty_cells       # Top-level data quality checker
└── README.md         # Project documentation
```

```plaintext
1.empty_cells
	Description: This script checks for missing data in the dataset and reports the number of empty cells per column.
	Usage : ./empty_cells <input_file_name>.txt
2.preprocess
	Description: Preprocess the dataset to prepare it for analysis. The script performs the following actions:
		Converts semicolon (;) separators to tab (\t).
		Converts Windows line endings (CRLF) to Unix line endings (LF).
		Converts decimal commas (e.g., 4,5) to decimal points (4.5).
		Removes non-ASCII characters.
    	Generates unique IDs for rows where the ID is missing.

	Usage : ./preprocess <input_file_name>.txt
3.analysis
	Description : Analyzes the cleaned dataset to answer the main four research questions.

	Usage : ./analysis <output_file_name>.tsv
```
Output

```plaintext
Example
The most popular game mechanics is Hand Management found in 48 games
The most game domain is Strategy Games found in 77 games

The correlation between the year of publication and the average rating is 0.226
The correlation between the complexity of a game and its average rating is 0.426
```