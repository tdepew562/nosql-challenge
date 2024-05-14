# nosql-challenge

This project involves analyzing food establishment data stored in a MongoDB database.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- You have installed Python (version 3.7 or higher) on your machine.
- You have installed MongoDB and started the MongoDB server.
  
If you encounter any issues during installation or setup, please refer to the documentation of Python and MongoDB for troubleshooting tips.

## Part 1: Database and Jupyter Notebook Set Up

1. **Import Data**: Import the data provided in the `establishments.json` file into MongoDB. Name the database `uk_food` and the collection `establishments`. Copy the text you used to import your data from your Terminal to a markdown cell in your notebook.

2. **Import Libraries**: Within your notebook, import the required libraries: PyMongo and Pretty Print (pprint).

3. **Mongo Client**: Create an instance of the Mongo Client.

4. **Confirm Database Setup**:
   - List the databases you have in MongoDB. Confirm that `uk_food` is listed.
   - List the collection(s) in the database to ensure that `establishments` is there.
   - Find and display one document in the `establishments` collection using `find_one` and display with `pprint`.
   - Assign the `establishments` collection to a variable to prepare the collection for use.

## Part 2: Update the Database

1. **Add New Restaurant**: Add a new restaurant named "Penang Flavours" to the database with specific details provided.

2. **Update BusinessTypeID**: Find the `BusinessTypeID` for "Restaurant/Cafe/Canteen" and update the new restaurant with the `BusinessTypeID`.

3. **Remove Dover Establishments**: Check how many establishments are in the Dover Local Authority, remove them from the database, and confirm deletion.

4. **Convert Number Values**: Convert certain number values stored as strings to numbers:
   - Use `update_many` to convert latitude and longitude to decimal numbers.
   - Use `update_many` to convert `RatingValue` to integer numbers.

## Part 3: Exploratory Analysis

Use the provided Jupyter Notebook (`NoSQL_analysis_starter.ipynb`) to perform the exploratory analysis.

### Questions to Explore:

1. **Hygiene Score of 20**: Which establishments have a hygiene score equal to 20?

2. **London Establishments with RatingValue >= 4**: Which establishments in London have a `RatingValue` greater than or equal to 4?

3. **Top Establishments with RatingValue of 5**: What are the top 5 establishments with a `RatingValue` of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?

4. **Local Authority with Hygiene Score of 0**: How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.

Use the provided notebook to answer these questions and provide the necessary information to the magazine editors.

## Acknowledgments

Special thanks to [ChatGPT](https://www.openai.com/gpt) for providing assistance and guidance during the development of this project.

Special thanks to Berkely Data Analytics for providing code snippets and resources used in this project. [UC Berkeley Extension](https://extension.berkeley.edu/)

## References

- UK Food Standards Agency (2022). [UK food hygiene rating data API](https://ratings.food.gov.uk/open-data/en-GB). Contains public sector information licensed under the [Open Government Licence v3.0](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/).
  Accessed Sept 9, 2022 and Sept 12, 2022 with the establishment settings as follows: longitude=51.5072, latitude=-0.1276, maxdistancelimit=4567, pagesize=10000, sortoptionkey=distance, pagenumber=(1,2,3,4,5,6,7,8).


Special thanks to the contributors of the [UCB-VIRT-DATA-PT-11-2023-U-LOLC](https://github.com/UCB-VIRT-DATA-PT-11-2023-U-LOLC) GitHub repository for providing valuable code and resources used in this project.

