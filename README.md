# nosql-challenge
Module 12 NOSQL Challenge : Evaluating ratings data from the UK Food Standards Agency for food magazine, Eat Safe, Love, to help their journalists and food critics decide where to focus future articles.
Module 12 Challenge: NoSQL Database Analysis
Overview
In this project, I analyzed food hygiene rating data from the UK Food Standards Agency for the magazine Eat Safe, Love. The dataset, provided in a JSON file (establishments.json), contains information about various food establishments across the United Kingdom. The project involved setting up a NoSQL database using MongoDB, performing data updates, and conducting exploratory analysis to answer specific questions posed by the magazine editors.

Repository Structure
The repository is organized as follows:

Copy
nosql-challenge/
│
├── Resources/                  # Folder containing the JSON data file
│   └── establishments.json
│
├── NoSQL_setup_starter.ipynb   # Jupyter Notebook for database setup and updates
├── NoSQL_analysis_starter.ipynb # Jupyter Notebook for exploratory analysis
└── README.md                   # Project documentation
Project Breakdown
Part 1: Database and Jupyter Notebook Set Up
Data Import: The establishments.json file was imported into MongoDB using the mongoimport command. The database was named uk_food, and the collection was named establishments.

Library Imports: Necessary libraries, including PyMongo and pprint, were imported.

Database Verification: The database and collection were verified by listing databases and collections, and a sample document was displayed using find_one().

Part 2: Update the Database
Insert New Restaurant: A new halal restaurant, "Penang Flavours," was added to the database.

Update BusinessTypeID: The BusinessTypeID for "Restaurant/Cafe/Canteen" was retrieved and updated for the new restaurant.

Remove Dover Establishments: All establishments in the Dover Local Authority were removed from the database.

Data Type Conversion: The latitude, longitude, and RatingValue fields were converted to appropriate data types (decimal and integer).

Part 3: Exploratory Analysis
The following analyses were performed to answer specific questions:

Establishments with a Hygiene Score of 20: Identified establishments with the worst hygiene score.

London Establishments with Rating >= 4: Found establishments in London with a high rating.

Top 5 Establishments Near "Penang Flavours": Identified the top-rated establishments closest to the new restaurant.

Local Authority Hygiene Analysis: Determined the number of establishments with a hygiene score of 0 in each Local Authority area, sorted by count.

Technologies Used
MongoDB: NoSQL database for storing and querying the data.

PyMongo: Python library for interacting with MongoDB.

Pandas: Used for data manipulation and analysis.

Jupyter Notebook: For code execution and documentation.

Installation and Setup
Clone this repository to your local machine.

Ensure MongoDB is installed and running on your system.

Import the establishments.json file into MongoDB using the mongoimport command.

Open the Jupyter Notebooks (NoSQL_setup_starter.ipynb and NoSQL_analysis_starter.ipynb) to execute the code and perform the analysis.

Results
The analysis provided insights into the UK food hygiene ratings, including:

Establishments with poor hygiene scores.

High-rated establishments in London.

Top-rated establishments near the newly added restaurant.

Local Authority areas with the most establishments having a hygiene score of 0.

Key Findings
41 establishments have a hygiene score of 20 (the worst possible score).

33 establishments in London have a rating of 4 or higher.

The top 5 establishments near "Penang Flavours" with a rating of 5 were identified.

The Local Authority area with the most establishments having a hygiene score of 0 is Thanet (1130 establishments).

Acknowledgements
UK Food Standards Agency for providing the dataset.

Instructors and TAs for guidance and support.

License
This project is licensed under the GNU GENERAL PUBLIC LICENSE.