# Student Data ETL Pipeline Using n8n

## 📌 Project Overview

This project demonstrates an automated **ETL (Extract, Transform, Load) pipeline** built using n8n to clean and process messy student enrollment data from a CSV file.

The workflow reads raw student data, cleans inconsistent values, standardizes email addresses and text fields, identifies invalid emails, removes duplicate records, filters students based on enrollment status, and exports the processed data to a CSV file.

## 🎯 Project Objectives

- Automate student enrollment data processing.
- Clean whitespace and inconsistent capitalization.
- Standardize email addresses.
- Identify invalid email addresses.
- Remove duplicate student records.
- Filter students based on enrollment status.
- Export the cleaned data as a CSV file.

## 🛠️ Tools and Technologies

- **n8n** — Workflow automation
- **JavaScript** — Data cleaning and transformation
- **CSV** — Input and output data format
- **Git and GitHub** — Version control and project hosting

## 🔄 ETL Workflow

### 1. Extract

- Start the workflow using a Manual Trigger.
- Read the raw student enrollment CSV file.
- Extract the CSV data into individual items for processing.

### 2. Transform

- Remove leading and trailing whitespace.
- Standardize student names, course names, and city names.
- Convert email addresses to lowercase.
- Validate email address formats.
- Mark invalid email addresses as `Invalid Email`.
- Standardize student enrollment dates.
- Remove duplicate student records according to the configured rules.

### 3. Filter

- Keep only student records that satisfy the selected enrollment-status rule.
- Exclude records that do not meet the filtering criteria.
- Handle missing or invalid email addresses according to the configured workflow rules.

### 4. Load

- Convert the processed student records into CSV format.
- Save the output to `binary-data.csv`.
- Verify the resulting data for consistency and readability.

## 📂 Project Structure

```text
student-data-etl-n8n/
├── .gitattributes
├── .gitignore
├── ELT AI Automation.json
├── Screenshot 2026-10-17 020929.png
├── binary-data.csv
└── student_enrollment_raw.csv
```

## 📄 File Descriptions

| File | Description |
|---|---|
| `.gitattributes` | Defines Git attributes for repository files. |
| `.gitignore` | Specifies files Git should ignore. |
| `ELT AI Automation.json` | Exported n8n workflow containing the ETL automation logic. |
| `Screenshot 2026-10-17 020929.png` | Screenshot documenting the n8n workflow. |
| `binary-data.csv` | Processed or cleaned student data exported by the workflow. |
| `student_enrollment_raw.csv` | Original student enrollment dataset containing messy records. |

## 🧹 Data Cleaning Rules

- Trim unnecessary spaces from text fields.
- Convert email addresses to lowercase.
- Validate email formatting and replace invalid addresses with `Invalid Email`.
- Standardize capitalization for names, courses, and cities.
- Identify duplicate records using the configured duplicate-detection rule.
- Retain only records matching the selected enrollment-status criteria.
- Preserve the original information when it is valid and available.

## 📊 Results

The pipeline is designed to reduce messy input data into a clean, structured CSV file suitable for further analysis.

The number of records removed depends on duplicate detection, missing or invalid data handling, and the enrollment-status filter.

**Input file:** `student_enrollment_raw.csv`

**Output file:** `binary-data.csv`

## ▶️ How to Run the Workflow

1. Download or clone this GitHub repository.
2. Open your n8n instance.
3. Import `ELT AI Automation.json` into n8n.
4. Ensure the input CSV file is available at the path configured in the workflow.
5. Update file paths and node settings if required by your environment.
6. Execute the workflow using the Manual Trigger.
7. Confirm that each node completes successfully.
8. Open `binary-data.csv` and verify the processed student records.

## 📸 Project Screenshot

The repository includes a screenshot of the n8n workflow:

`Screenshot 2026-10-17 020929.png`

The screenshot documents the workflow setup and can be used to review the automation process.

## 📚 Key Learnings

- Understanding the ETL process: Extract, Transform, and Load.
- Building automated data-processing workflows in n8n.
- Using JavaScript to clean and validate CSV data.
- Detecting invalid email addresses and duplicate records.
- Applying filtering rules to student enrollment data.
- Exporting structured data into CSV format.
- Managing and sharing project files using GitHub.

## 🚀 Future Improvements

- Generate a separate file for records requiring manual review.
- Improve duplicate detection using student IDs and normalized emails.
- Add more comprehensive data validation.
- Generate an automated processing summary with input and output counts.
- Schedule the workflow to process new enrollment files automatically.

## 👤 Author

**sivakumar**

## 📄 License

This project was created for educational and learning purposes.
