
---------------------------------------------------------------------------------------------------
                                    INSTRUCTIONS FOR USE 
---------------------------------------------------------------------------------------------------

1º) Install the R and R Studio software;

2º) Click on the .Rproj file named '1_PROJECT__RMask_Anonimizer' to open R Studio;

2º) Click and open the .Rmd file named '2_INSTALL__R_packages' and install the 
packages by clicking on the button labeled 'Run Current Chunk' available in the 
chunk of this file;

3º) Close the file '2_INSTALL__R_packages';

4º) Place the data file in csv or xls or xlsx format in the '1_Dataset' folder;

5º) Click and open the .Rmd file named '3_SCRIPT__RMask_Anonimizer', fill in the requested 
information (about the settings and the study) and click the 'Knit' button;

6º) Wait for the HTML report to be generated in the folder named;

7º) A file with the suffix "..._MASK" will be exported to the "1_Dataset" folder, 
    containing the anonymized dataset. The column that contains the identifier to 
    be anonymized will be renamed to "ID HASH".;

8º) End.

---------------------------------------------------------------------------------------------------
                                    ABOUT RMask Anonimizer Tool
---------------------------------------------------------------------------------------------------

The RMask Anonimizer tool, based on the provided script, performs the following analysis steps:

1. Initial Settings:

- Sets a secret key (secret_key) for hashing purposes.
- Specifies the dataset file name (File_name) and the columns that will be anonymized 
  (IdentifierColumn and Column_age).
- Determines the format of the dataset file (CSV, XLSX, or XLS).

2. Package Installation:

- Checks and installs the necessary R packages, such as "digest", "readr", "dplyr", among others.

3. File Type Determination:

- Identifies the file type based on user input (CSV, XLSX, or XLS).

4. File Path Configuration:

- Sets the path to read the dataset and save the anonymized version.

5. Data Loading:

- Loads the dataset based on the determined file type.

6. Data Anonymization:

- Anonymizes the specified columns by replacing them with a hashed version. 
  If the "Age" column is present, it's combined with the "IdentifierColumn" to create a 
  combined value before hashing.
- The original identifier column is replaced with the hashed version and renamed to "ID HASH".

7. Display of Anonymized Dataset:

- Displays the first 100 rows of the anonymized dataset in a table format.

8. Data Export:

- Saves the anonymized dataset to the specified path.

9. Performance Tracking:

- Displays the start and end times to track the performance of the script.


In summary, the RMask Anonimizer tool is designed to anonymize specific columns in a dataset 
by replacing identifiable values with unique hashes, thus ensuring data privacy.

---------------------------------------------------------------------------------------------------
email:labrgrupo@gmail.com