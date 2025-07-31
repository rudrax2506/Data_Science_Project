## Friend & Page Recommendation System (Python)
This project provides a set of Python scripts to load, clean, and analyze a social network dataset stored in JSON format. It includes functionality to display users and their connections, clean the data, suggest potential friends based on mutual connections, and recommend pages users may like.

## Features
### ✅ Display Users and Pages
Lists all users with their IDs, friends, and liked pages, along with available pages and their names.

### ✅ Data Cleaning
- Removes users with missing names
- Removes users without any friends or liked pages
- Eliminates duplicate entries in friends lists
- Removes duplicate pages by ID

### ✅ People You May Know
Recommends new friends to each user based on mutual friends. Users are not recommended if they are already friends or if they are the user themselves.

### ✅ Pages You Might Like
Recommends new pages to users based on shared interests with others. If a user's friends have liked a page that the user hasn't, it is scored and suggested.

## Files
- `data2.json`: Raw social network data (used for display and cleaning)
- `cleaned_data2.json`: Output of the cleaned data
- `data.json`: Structured or cleaned dataset used for recommendation functions

## Output
The output for all the code files is:

File_1:
Users and Their Connections:
Amit (ID: 1) - Friends: [2, 3] - Liked Pages: [101]
Priya (ID: 2) - Friends: [1, 4] - Liked Pages: [102]
Rahul (ID: 3) - Friends: [1] - Liked Pages: [101, 103]
Sara (ID: 4) - Friends: [2] - Liked Pages: [104]

Pages:
101: Python Developers
102: Data Science Enthusiasts
103: AI & ML Community
104: Web Dev Hub

File_2:
{
 "users": [
  {
   "id": 1,
   "name": "Amit",
   "friends": [
    2,
    3
   ],
   "liked_pages": [
    101
   ]
  },
  {
   "id": 2,
   "name": "Priya",
   "friends": [
    1,
    4
   ],
   "liked_pages": [
    102
   ]
  },
  {
   "id": 4,
   "name": "Sara",
   "friends": [
    2
   ],
   "liked_pages": [
    104
   ]
  }
 ],
 "pages": [
  {
   "id": 101,
   "name": "Python Developers"
  },
  {
   "id": 102,
   "name": "Data Science Enthusiasts"
  },
  {
   "id": 103,
   "name": "AI & ML Community"
  },
  {
   "id": 104,
   "name": "Web Development"
  }
 ]
}

File_3:
People You May Know for User 1: [7, 8, 9, 10, 11, 12]
People You May Know for User 2: [4, 8, 10, 11, 12, 9, 13]
People You May Know for User 3: [6, 5, 9, 13, 10, 14]
People You May Know for User 4: [2, 7, 5, 10, 12, 14, 11, 15]
People You May Know for User 5: [12, 3, 4, 9, 7, 8, 16, 14, 17]
People You May Know for User 6: [3, 10, 11, 7, 8, 9, 13, 18]
People You May Know for User 7: [4, 1, 10, 14, 15, 5, 6, 11, 12, 19]
People You May Know for User 8: [9, 1, 2, 13, 16, 6, 5, 12, 11, 20]
People You May Know for User 9: [8, 3, 13, 5, 12, 16, 17, 1, 6, 2, 14, 21]
People You May Know for User 10: [11, 6, 4, 7, 14, 15, 18, 1, 2, 3, 13, 22]
People You May Know for User 11: [10, 6, 15, 13, 18, 1, 2, 4, 7, 8, 16, 20, 19, 23]
People You May Know for User 12: [5, 9, 16, 14, 17, 1, 2, 4, 8, 7, 15, 19, 20, 24]
People You May Know for User 13: [8, 9, 11, 16, 20, 17, 21, 2, 3, 6, 10, 18, 25]
People You May Know for User 14: [7, 10, 12, 15, 19, 18, 22, 3, 4, 5, 9, 17, 26]
People You May Know for User 15: [19, 7, 10, 11, 14, 18, 22, 23, 4, 12, 27]
People You May Know for User 16: [20, 8, 9, 12, 13, 17, 21, 24, 5, 11, 28]
People You May Know for User 17: [21, 9, 12, 13, 16, 20, 24, 25, 5, 14, 29]
People You May Know for User 18: [22, 10, 11, 14, 15, 19, 23, 26, 6, 13, 30]
People You May Know for User 19: [15, 23, 14, 18, 22, 26, 27, 7, 12, 11, 1]
People You May Know for User 20: [16, 24, 13, 17, 21, 25, 28, 8, 11, 12, 3]
People You May Know for User 21: [17, 25, 13, 16, 20, 24, 28, 29, 9, 5]
People You May Know for User 22: [18, 26, 14, 15, 19, 23, 27, 30, 10, 7]
People You May Know for User 23: [19, 27, 11, 15, 18, 22, 26, 30, 1, 9]
People You May Know for User 24: [20, 28, 16, 17, 21, 25, 29, 12, 3, 13, 15]
People You May Know for User 25: [21, 3, 5, 17, 20, 24, 29, 28, 2, 4, 6, 13]
People You May Know for User 26: [22, 1, 7, 18, 19, 23, 30, 27, 2, 4, 8, 14]
People You May Know for User 27: [23, 1, 11, 19, 22, 26, 30, 2, 6, 10, 15, 7, 9]
People You May Know for User 28: [24, 3, 13, 20, 21, 25, 29, 2, 8, 9, 16, 5, 15]
People You May Know for User 29: [15, 5, 17, 21, 24, 25, 28, 4, 7, 10, 12, 14, 13]
People You May Know for User 30: [7, 9, 22, 23, 26, 27, 12, 14, 19, 16, 17, 21, 18, 11]

File_4:
Recommendations for Amit (User ID: 1):
  - Page ID 103 (Score: 2)
  - Page ID 105 (Score: 1)
  - Page ID 107 (Score: 1)

Recommendations for Priya (User ID: 2):
  - Page ID 101 (Score: 2)
  - Page ID 105 (Score: 1)
  - Page ID 108 (Score: 1)

Recommendations for Rahul (User ID: 3):
  - Page ID 102 (Score: 2)
  - Page ID 107 (Score: 1)
  - Page ID 108 (Score: 1)

Recommendations for Sara (User ID: 4):
  - Page ID 109 (Score: 1)

Recommendations for Neha (User ID: 5):
  - Page ID 101 (Score: 1)
  - Page ID 103 (Score: 1)
  - Page ID 111 (Score: 1)

Recommendations for Vikram (User ID: 6):
  - Page ID 113 (Score: 1)

Recommendations for Kunal (User ID: 7):
  - Page ID 102 (Score: 1)
  - Page ID 103 (Score: 1)
  - Page ID 115 (Score: 1)

Recommendations for Anjali (User ID: 8):
  - Page ID 101 (Score: 1)
  - Page ID 102 (Score: 1)
  - Page ID 117 (Score: 1)

Recommendations for Ravi (User ID: 9):
  - Page ID 119 (Score: 1)

Recommendations for Sneha (User ID: 10):
  - Page ID 121 (Score: 1)

Recommendations for Arjun (User ID: 11):
  - Page ID 102 (Score: 1)
  - Page ID 123 (Score: 1)

Recommendations for Meera (User ID: 12):
  No new page recommendations found.

Recommendations for Kabir (User ID: 13):
  No new page recommendations found.

Recommendations for Tanya (User ID: 14):
  No new page recommendations found.

Recommendations for Varun (User ID: 15):
  - Page ID 101 (Score: 1)

Recommendations for Rhea (User ID: 16):
  No new page recommendations found.

Recommendations for Ishan (User ID: 17):
  - Page ID 103 (Score: 1)

Recommendations for Simran (User ID: 18):
  No new page recommendations found.

Recommendations for Pooja (User ID: 19):
  - Page ID 104 (Score: 1)

Recommendations for Yash (User ID: 20):
  No new page recommendations found.

Recommendations for Ananya (User ID: 21):
  No new page recommendations found.

Recommendations for Dev (User ID: 22):
  No new page recommendations found.

Recommendations for Aditi (User ID: 23):
  - Page ID 105 (Score: 1)

Recommendations for Rohan (User ID: 24):
  No new page recommendations found.

Recommendations for Nisha (User ID: 25):
  No new page recommendations found.

Recommendations for Gautam (User ID: 26):
  No new page recommendations found.

Recommendations for Kriti (User ID: 27):
  - Page ID 106 (Score: 1)

Recommendations for Harsh (User ID: 28):
  No new page recommendations found.

Recommendations for Naveen (User ID: 29):
  No new page recommendations found.

Recommendations for Ishita (User ID: 30):
  No new page recommendations found.
