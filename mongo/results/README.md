# Fun Facts
  ## Patrons in Total
      Adult: 271,588
      Juvenile: 58,767
      Senior: 47,366
      Teen: 40,340
      Welcome: 10,587
      Digital Access: 3,707
      Teacher: 3,161
      Staff: 808
      Retired Staff: 209
      At User Adult: 128
      Library by Mail: 117
      Visitor: 111
      Bibliocommons: 109
      At User Senior: 76
      At User Welcome: 14
      At User Teen: 10
      At User Juvenile: 9
      Business: 8 
      
      Total: 437,115 records

  ## Juvenile
    Highest total checkouts: 6,148
    Highest total renewals: 4,432

  ## Teen
    Highest total checkouts: 8,366
    Highest total renewals: 5,228
    
  ## Adult
    Highest total checkouts: 45,380
    Highest renewals: 10,801

  ## Senior
    Highest total checkouts: 22,474
    Highest total renewals:  11,321

# Runtime Stats
Query execution time for Adult records: 381 ms (271,588 records)

# Reflection
After learning from my old mistakes, I started this project early and got better results. In general, MongoDB was more user-friendly compared to MySQL. I didn't have too many problems, other than having to research how to query searches. One thing I enjoyed about MongoDB was how easy importing a CSV file was. With MySQL, I encountered many problems. However, for this project, the file was uploaded within seconds. MongoDB is also intuitive and can determine data types correctly (usually). I found MongoDB fun and thought it was organized better than MySQL. 

To sum it up, I made my database better. Before, my database was not as organized. I tried to develop this concept of separating patrons by either age or their special role. This was because the Excel spreadsheet oddly organized patrons by either age or role. In my old database, if a patron was classified by their age, they received an age role, but not a special role. If a patron was classified by a special role (e.g., Bibliocommons), then they received a special role, but not an age role. I also previously determined the age ranges with min and max age, then assigned the age group labels. However, for this project, I changed a few things. 

To organize the age groups, I first determined all the distinct age ranges by using MongoDB. Since each age range was written as a string in the file, I didn’t need to overcomplicate the process. Instead of manually calculating ranges like before, I simply mapped each distinct string to its corresponding age group label. For example, an adult had these distinct age ranges: 

    20 to 24 years
    25 to 34 years
    35 to 44 years
    45 to 54 years
    55 to 59 years
    60 to 64 years

If a patron’s age range matched one of these values, they received the “Adult” label. You could imagine how messy this was in MySQL. To classify patrons as the "Adult" label, I had to define a minimum age of 20 and a maximum age of 64. If a patron’s age range fell within those bounds, they were labeled “Adult.” In theory, that should have worked, but then came the “At User” patrons. They were a special case, requiring both a role and an age range. Remember, I tried separating patrons by either age or special role. This was a great improvement! In my previous project, one tricky edge case was that a patron could be classified as a teacher, yet MySQL would still assign their age as “Unknown.” I also wanted to correct any errors in the data (such as a 70-year-old Juvenile?!). Best of all, I introduced membership types to replace roles. Now, each patron is linked directly to a specific type of membership card. For example, an adult patron might have a profile like this: 

### Old Profile Example #1
    Age Group: Adult
    Patron Type Definition: Adult
    Role Type: Adult

### New Profile Example #1
    Age Group: Adult
    Patron Type Definition: Adult
    Membership Type: Standard Adult Card

### New Profile Example #2
    Age Group: Senior
    Patron Type Definition: Staff
    Membership Type: Staff Card

Though it is still a bit redundant, at least it's not too bad. 

Another important consideration was how to uniquely identify patrons. In a library setting, a staff member can typically look up a patron by their ID, so I wanted to implement a Patron ID. In my earlier attempt, I used auto‑increment in MySQL. For this database, I used MongoDB's object ID. By taking just the last eight characters, I created IDs that look more authentic and are visually cleaner. Lastly, I added sorting features. Results can be organized by Patron ID, Checkout Total, or Renewal Total in either ascending or descending order.

# Future Improvements Ideas
    Less redundant labeling (e.g., age group, patron type definition, membership type)
    Better-looking search bar/dropdown boxes (looks ancient and messy at the moment)
    Better profiles + features such as photos
    More testing/debugging
    
