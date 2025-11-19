# App Description
This app allows you to search for a patron via patron ID, age group, membership type, active month, or library.  

# Features
This app allows you to organize your results by patron ID ascending/descending, checkout total ascending/descending, or renewal total ascending/descending. 
 
 If you use the search bar:
  - You can only search a patron's ID. This ID is from MongoDb's object id.
  - The _id is shortened (8 characters) for easy searching.
  - Press "Clear" to return to the home page or the "Back to Home Page" button.

 If you use the dropdown box,
  - You can select your desired search queries.
  - The search will look for any patrons that fit the search query.
      - e.g., Adult, March, Anza
  -  Press "Clear" to return or the "Back to Home Page" button.

# Profile 
Each patron has a profile that includes the following information:
  - Patron ID
  - Checkout Total
  - Renewal Total
  - Patron Type Code
  - Patron Type Definition
  - Age Range
  - Age Group
  - Membership Type
  - Home Library Code
  - Home Library Definition
  - Within SF County (yes/no)
  - Notification Medium Code
  - Notification Definition
  - Circulation Active Month
  - Provided Email Address (yes/no)
