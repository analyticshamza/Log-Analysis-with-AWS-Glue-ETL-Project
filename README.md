# 🚀 Log Analysis ETL Pipeline using AWS Glue

A hands-on data engineering project to parse raw log files using **AWS Glue**, **Amazon S3**, and **Regex extraction**. This project simulates real-world log processing for an e-commerce platform — converting raw unstructured log data into clean, structured CSV format for monitoring and analysis.

---

---

## 📌 Project Objectives

- 📁 **Extract**: Load a raw log file stored in Amazon S3
- 🧪 **Transform**: Use AWS Glue + Regex to split logs into 3 fields
- 📤 **Load**: Output a clean CSV back into S3

---

## 🛠️ Tools & Technologies

| Service         | Purpose                         |
|-----------------|----------------------------------|
| 🪣 Amazon S3     | Store input and output files     |
| 🧪 AWS Glue      | ETL pipeline & job orchestration |
| 🧹 Regex Extractor | Transform raw text into columns |
| 🔐 IAM Role      | Permission management            |
| 📊 Excel         | View results for validation      |

---

## 📁 Project Structure

📦 ETL-Log-Analysis/
├── systemLog.csv # Raw input data (logs)
├── output.csv # Transformed output
├── etl_screenshot.png # AWS Glue pipeline visual
├── excel_output.png # Before & after comparison
└── README.md # Project documentation

---

## 🔁 ETL Flow Summary

1. **Upload** `systemLog.csv` to S3
2. **Catalog** using AWS Glue Crawler
3. **Create ETL Job** (Visual Editor)
4. **Apply Regex** to `text` column:
5. **Extract Columns**:
- `Level`
- `Message`
- `Source`
6. **Write to S3** as clean `CSV`

---

## 🧪 Sample Data

### 🔹 Input (Raw Log File)

| Timestamp         | Text                                        | LogCode |
|------------------|---------------------------------------------|---------|
| 29-03-2024 10:15 | INFO\|User logged in successfully\|Auth     | 200     |
| 29-03-2024 10:17 | ERROR\|Database connection failed\|Database | 300     |

---

### 🔸 Output (After ETL)

| Timestamp         | Text                                        | LogCode | Level | Message                    | Source   |
|------------------|---------------------------------------------|---------|-------|----------------------------|----------|
| 29-03-2024 10:15 | INFO\|User logged in successfully\|Auth     | 200     | INFO  | User logged in successfully | Auth     |
| 29-03-2024 10:17 | ERROR\|Database connection failed\|Database | 300     | ERROR | Database connection failed | Database |

---

## 📸 Screenshots

| Glue ETL Visual Job | Input vs Output (Excel) |
|---------------------|-------------------------|
| ![Glue ETL](![Image](https://github.com/user-attachments/assets/68851ff5-a872-44ab-a020-c8a9ba350c8e)) |
| ![Excel Raw_Uploaded](![Image](https://github.com/user-attachments/assets/899b5b3e-d6ca-4b44-a82e-05aee54cdea4)) |
| ![Excel Output](![Image](https://github.com/user-attachments/assets/cefac3c1-f9d6-4012-9c86-dfcf6a9f986b)) |

---

---

## 🙋‍♂️ Author

**Ali Hamza**  
*Aspiring Data Analyst*

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).





