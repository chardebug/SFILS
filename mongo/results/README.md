# Fun Facts
  ## Patrons in Total
      - Adult: 271,588
      - Juvenile: 58,767
      - Senior: 47,366
      - Teen: 40,340
      - Welcome: 10,587
      - Digital Access: 3,707
      - Teacher: 3,161
      - Staff: 808
      - Retired Staff: 209
      - At User Adult: 128
      - Library by Mail: 117
      - Visitor: 111
      - Bibliocommons: 109
      - At User Senior: 76
      - At User Welcome: 14
      - At User Teen: 10
      - At User Juvenile: 9
      - Business: 8 
      - Total: 437,115 records

  ## Juvenile
    - Highest total checkouts: 6,148
    - Highest total renewals: 4,432

  ## Teen
    - Highest total checkouts: 8,366
    - Highest total renewals: 5,228
    
  ## Adult
    - Highest total checkouts: 45,380
    - Highest renewals: 10,801

  ## Senior
    - Highest total checkouts: 22,474
    - Highest total renewals:  11,321

# Runtime Stats
Query execution time for Adult records: 381 ms (271,588 records)

# Reflection
After learning from my old mistakes, I started this project early and got better results. In general, MongoDB was more user-friendly compared to MySQL. I didn't have too many problems, other than having to research how to query searches. One thing I enjoyed about MongoDB was how easy importing a CSV file was. With MySQL, I encountered many problems. However, for this project, the file was uploaded within seconds. MongoDB is also intuitive and can determine data types correctly (usually). I found MongoDB fun and thought it was organized better than MySQL. 

I made my database better. Before, my database was not as organized. I tried to develop this concept of age and special roles. The Excel spreadsheet oddly organized patrons by either age or a type of role. In my old database, if a patron was simply classified by their age, they did not receive a special role. If a patron was classified by a role (e.g., Bibliocommons), then they were labeled with the special role. I also tried to label the age ranges properly by determining the range, then assigning the age range label. However, for this project, I changed a few things. 

To help classify age ranges, I looked at all the distinct age ranges in MongoDB. Then, I made sure that these distinct age ranges were labeled properly. The "Adult" label had many entries/ranges, so I made sure these age ranges were labeled properly. Once I did this, it was easy to determine how old the patron was. 

Previously, I had an issue with the special roles. A patron might be a teacher, but MySQL classified their age as "Unknown." In this database, a patron will have their age range and their patron type stated in their profile. Best of all, I implemented membership types, which replaced roles. Like in a real library, a patron is linked to a certain type of card. I did this because I realized how unorganized my profiles looked. For example, an adult could have this profile: 

## Profile
  - Age Group: Adult
  - Patron Type Definition: Adult
  - Role Type: Adult

Instead, I changed the profiles to look like this:

## Profile
  - Age Group: Adult
  - Patron Type Definition: Adult
    Membership Type: Standard Adult Card

## Profile
  - Age Group: Senior
  - Patron Type Definition: Staff
  - Membership Type: Staff Card

Another feature I added to make the app more user-friendly was profiles. The profiles showcase the full information of a patron. Another feature I added was organizing Patron ID, Checkout Total, and Renewal Total ascending/descending. This is a nice feature. You can search for a specific type of patron and then organize the results by either Patron ID, Checkout Total, or Renewal Total. Lastly, of course, I implemented Patron ID. I did have a Patron ID before in my old database, but this was done with auto-increment. For this database, I took advantage of MongoDB's object ID and decided to just use the last 8 characters as the ID. 
