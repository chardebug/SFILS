# Database Scripts

This folder contains all the initialization scripts that helps us (perhaps convert and) load the Excel sheet into the database tables.

The scripts that are used to modify (indexing, moving, updating, data cleaning, ...) the database tables (after the data is loaded into the database) are also included here.

# Methods
What was something new I added? I noticed a lot of the patrons were grouped by either age or special role. Therefore, I thought it would be nice to group the patrons in a different way.
That is why I made age and role important. A patron can be classified as a Juvenile, Teen, Adult, or Senior based on their patron code. But if they are not classified that way, I made
them classified into their different roles such as "Welcome," "Staff," "Visitor," and "Business."

I inserted a lot of the data into the tables, such as the library codes, to ensure easier importing. I also modified the CSV file. 

What I found most difficult was the age and roles being tied together. Therefore, I don't feel too successful in the way I arranged things, but it looks prettier than my last attempt.

# Future Improvements and Wishes
- Better organization (SQL in general)
- Prettier app (More options, profiles, avatars, etc.)
- Improve role_id, age_range_label, age_id, etc.
- Minimize null values/blank entries
- Polish mistakes in the .csv file. A 70+ year old juvenile...? Heh. Odd. 

# Reflection
The first time I submitted this, I rushed to get it done. I went to bed that night feeling ashamed. Wow, I really uploaded that onto GitHub! My SQL database was a total mess. I decided
to take the penalty and go back. I had to redo it! Therefore, I spent the whole day redoing it. Do I feel better? Tremendously. I have also learned a lot. SQL is no joke, at times. I had
 some fits of rage (I get ragebaited easily). But, I feel proud that I decided to try again. I learned so much! I am more proud of the work I've done, and I hope people can see it. I am
inspired to do more database practice. This was quite fun, but I MUST say... maybe I should manage my time better! 
