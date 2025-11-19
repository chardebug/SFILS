
#  Installation 
1. Download <a href="https://www.mongodb.com/try/download/database-tools">MongoDB Database Tools</a>.
2. Extract the ZIP file to your desktop. You might want to rename the folder to something simple like `mongodb-tools`.
   ```bash
   C:\Users\<YourUsername>\Desktop\mongodb-tools\`)
4. After extracting the ZIP file, open Command Prompt.
5. Navigate to the `bin` folder inside the extracted tools directory:
   ```bash
   cd "C:\Users\<YourUsername>\Desktop\mongodb-tools\bin"
6. Verify installation inside the bin folder.
   ```bash
   mongoimport --version
7. Download the CSV file and extract the ZIP file to your desktop. 
8. Import the CSV file into MongoDB using:
   ```bash
   mongoimport --db SF_LibraryDB --collection Patron --type csv --headerline --file "C:\Users\<YourUsername>\Desktop\SFPL_Data_Fixed.csv"
9. Open MongoDB and verify everything is imported correctly. 
