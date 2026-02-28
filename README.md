<img width="361" height="249" alt="wareflow_logo" src="https://github.com/user-attachments/assets/aafe0697-7f24-41db-a516-d992057c71aa" />

--- 

# Requirements and Goals

This app was designed to assist users manage warehouse inventory. It was designed with small business owners in mind <br>
It is a simple and powerful app that allows users to: <br>

- **Add inventory** items,
- **Adjust Inventory** counts,
- **Remove Inventory** items,
- **View All Items** in a single warehouse <br>

In addition to these features, users will get SMS Messages when inventory levels drop to zero.

# Meet the APP

### To meet the requirements, there were several screens that needed to be created:

I created a **Dashboard** that the user will first see after the sign in screen. Here they are able to get to any function of the app. <br>

<img width="356" height="750" alt="image" src="https://github.com/user-attachments/assets/c3a53cec-9c3d-4372-b610-c782fa133d62" /> <br>

---

Users needed to be able to see a list of all inventory items. For this a view that displays a rolling list of inventory <br>
including **Item Name / Number**, a **description** and **stock quantity** for each item. Also in each row is a link to edit any item.<br>

<img width="356" height="750" alt="image" src="https://github.com/user-attachments/assets/1e33eda1-0665-49d6-b241-f6e86d6cf30d" /> <br>

---

Adding / Updating an item screen allows the user to add or modify an item. Here they need to add an Item Number, Description and initial inventory quantity.

<img width="356" height="750" alt="image" src="https://github.com/user-attachments/assets/279b2d9e-0825-4c23-8e08-3062f878b1d8" /> <br>

---

Users can remove or adjust inventory counts for any item:

<img width="356" height="750" alt="image" src="https://github.com/user-attachments/assets/734dcc5d-37c0-4e05-bf1c-b5eb21d06eff" />   
<img width="356" height="750" alt="image" src="https://github.com/user-attachments/assets/65531130-40a6-460d-bfeb-32bdb8ec9a30" /> <br>

---

From anywhere in the app, users can navigate from the three dot menu bar on the top right of the app. 

<img width="356" height="750" alt="image" src="https://github.com/user-attachments/assets/2818bac4-1d10-4040-9444-7b02a19b77f1" /> <br>

---

Throughout testing each feature, I kept thinking as a user. The "what if I wanted to do..." was always in the forefront of my thinking as I was testing each screen.
Thinking as a user helps to identify any pitfalls that may come up. For instance, when a user adds a new item if the fields remained populated, the user would be 
unsure if the item was actually added. Even with a prompt, clearing the fields and putting the cursor back to the Item field gave a better sense of success. <br>

I feel these designs were successful because each screen had a singular purpose. It made the logic behind each screen cleaner knowing its intent and the expected outcome. 

# Coding it....

Coming from a background in UI design, mostly in Eclipse WindowBuilder, I understood the basics behind adding elements with functions and creating events linking to buttons and Edit Text fields. <br>

That being said, this app I had to take a different approach. Once I understood what screens I needed, and the layouts were set I worked on creating the activities for each layout.<br>

I created one activity at a time. Made sure I had all the controls and functions I needed for each. Once I was happy with the base functionality, I started putting together the Intent calls for each activity.
That way I knew each activity worked independently. I apply this rule today with incremental coding. I'll generate a small series of logic and test to make sure it works. So when things go belly up, it'll be a 
smaller set of code to check rather than trying to debug an entire program.

# Functional Testing

For each major function in the activities, I ran it through the emulator. I ran several tests for each activity trying to think of all the edge cases that could come up. Like if a user is trying to delete an item but enters a 
part number that doesn't exists. Or enters no part number at all. Doing this in an incremental way worked the best for me. <br>

I also leaned on LogCat for a lot of the debugging. It helped to have a live stream of what the app was doing and where it was failing. Even when the app didn't look like it was failing on the emulator. 

# Overcoming Challenges

On a UI standpoint, one of the bigger challenges was getting the WYSIWYG from Android Studio to the phone. I had to understand where Themes would override background colors and tints. <br>

For coding, the Recycler View was a challenge to understand and get to work. Just displaying the text in the View was not the challenge, it was when I added the Edit button for each row. I needed to find a way that 
referenced each row as an object that contained each field to call back on the next activity. 

# Showcase

The login screen was one of the pieces that I feel has a strong working logic behind it. There were a lot of scenarios to consider when a user is first faced with the app. 

- Do they have an existing account?
- Have they entered the right password?
- Does the app have SMS permissions set?

These are some of the same types of checks we do today, where its checking security tables to make sure users have access to run a particular program or report. <br>
User validation is a big part of my world, so this piece came natural (other than storing passwords in plain text :) )
