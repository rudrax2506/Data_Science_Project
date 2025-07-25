🔍 JSON Data Cleaning and Recommendation System in Python

📌 Project Overview
This is a data science mini-project focused on performing data cleaning and building a simple recommendation system using only Python and a JSON dataset. The project demonstrates how to process and clean nested JSON data, remove duplicates, filter out incomplete records, and implement basic friend and page suggestions — entirely without external libraries.

🧠 Key Objectives:
Load and parse JSON data.
Clean the dataset by:
  Removing users with no friends.
  Removing duplicate entries (like duplicate page IDs or user names).
  Handling missing or empty fields (like blank names).
Implement functionality to:
  Suggest "People You May Know" for a given user.
  Recommend "Pages You May Like" for a given user.

📁 Dataset Sample
The JSON file used in this project contains users and pages information in the following format:
{
    "users": [
        {"id": 1, "name": "Amit", "friends": [2, 3], "liked_pages": [101]},
        {"id": 2, "name": "Priya", "friends": [1, 4], "liked_pages": [102]},
        {"id": 3, "name": "", "friends": [1], "liked_pages": [101, 103]},
        {"id": 4, "name": "Sara", "friends": [2, 2], "liked_pages": [104]},
        {"id": 5, "name": "Amit", "friends": [], "liked_pages": []}
    ],
    "pages": [
        {"id": 101, "name": "Python Developers"},
        {"id": 102, "name": "Data Science Enthusiasts"},
        {"id": 103, "name": "AI & ML Community"},
        {"id": 104, "name": "Web Dev Hub"},
        {"id": 104, "name": "Web Development"}
    ]
}

 Features
✅ Clean malformed or duplicate entries
✅ Remove users with no friends
✅ Suggest potential friends based on mutual connections
✅ Recommend pages based on mutual interests

🚧 Project Status
Currently In Progress
I'm just getting started with this project and will update the repository with each feature I implement. Stay tuned for commits, code improvements, and possible visualizations!
