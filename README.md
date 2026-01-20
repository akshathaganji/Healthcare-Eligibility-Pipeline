# Healthcare-Eligibility-Pipeline
# Overview
This project demonstrates a scalable, configuration-driven data ingestion pipeline for processing member eligibility files from multiple healthcare partners.
Each partner may provide files with different delimiters, column names, and date formats.
The pipeline standardizes all inputs into a unified schema ready for downstream consumption.
The solution is implemented using Python and Pandas within a Jupyter Notebook, emphasizing readability, maintainability, and minimal code changes when onboarding new partners.

# Output Fields
external_id :	Partner-specific unique member identifier

first_name	:Title case

last_name :	Title case

dob:	ISO-8601 format (YYYY-MM-DD)

email:	Lowercase

phone :	Formatted as XXX-XXX-XXXX

partner_code :	Hardcoded identifier for the source partner

# Running the Pipeline

# Prerequisites
  a.Python 3.8 +

  b.Pandas

  # Steps
   a. Ensure the necessary sample input files are in the same directory

   b.Running all cells

  # Adding a New Partner:
    To onboard a new partner,
    a.Add a new entry to PARTNER_CONFIG
    b. Specify : File Path, Delimiter, Column Mappings, Date Formats, Partner Code
    c. No changes to core processing logic are required
  
  # Future Enhancements
    -Schema Validation

    -Automated Unit Testing

    -Migration to PySpark for large-scale processing
  
