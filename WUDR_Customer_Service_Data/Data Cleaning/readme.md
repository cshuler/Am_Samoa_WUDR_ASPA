# Water Data File Management and Processing Tool

This tool provides a suite of file management and data processing utilities, specifically tailored for handling water usage data in spreadsheet formats. Its primary functions include organizing data, cleaning data, filtering, and transforming data into a specific format.

## Features:

1. **File Management:** 
    - Delete directories and their contents.
    - Copy files from one directory to another.
    - Delete non-spreadsheet files from a directory.
    - Rename files by replacing month names with numerical representation.
    - Delete files with names longer than a specific length.
    - Rename files based on their date format.
    - Remove all sheets except the second one in each Excel file.

2. **Data Processing:** 
    - Load and combine multiple spreadsheet files.
    - Export data to a CSV file.

3. **Data Cleaning:** 
    - Load data with specified memory considerations.
    - Clean up data, handle missing values, and adjust data types.
    - Filter data based on specific criteria.
    - Map data attributes to specific categories.
    - Transform data into a desired format.

## Usage:

**File Management:**

Use the `FileManager` class for all file-based operations:

```py
FileManager.delete_directory("path_to_directory")
FileManager.copy_files("source_directory", "destination_directory")
FileManager.delete_non_spreadsheet_files("directory_path")
FileManager.replace_month_names_in_files("directory_path")
FileManager.delete_files_with_long_names("directory_path")
FileManager.rename_dates_in_files("directory_path")
FileManager.remove_all_but_second_sheet_in_xlsx("directory_path")
```

**Data Processing and Cleaning:**

For data operations, use the `DataProcessor` and `DataCleaner` classes:

```py
combined_data = DataProcessor.load_and_combine_files("directory_path")
DataProcessor.export_to_csv(combined_data, "output_path")

cs_data = DataCleaner.load_data("file_path")
cs_data = DataCleaner.clean_data(cs_data)
cs_data = DataCleaner.filter_for_residential(cs_data)
cs_data = DataCleaner.map_rsp_to_beneficial_use_category(cs_data)
cs_data = DataCleaner.transform_to_site_specific_format(cs_data)

DataProcessor.export_to_csv(cs_data, "output_path")
```

## Dependencies:

- `os`
- `glob`
- `re`
- `shutil`
- `pandas`
- `openpyxl`

Ensure you have these libraries installed to use this tool.

## Notes:

- Before running the script, backup your data as the tool can delete or modify files and directories.
- Always validate the results after processing to ensure data integrity and correctness.

