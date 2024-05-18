# NoSQL Challenge
From Module 12: NoSQL Databases from the Data Analytics Boot Camp by Monash University and EdX.

By implementing skills learnt throughout the module, an attempt at the challenge has been submitted here.

## Contents
- Resources folder
    - `establishments.json` file
- 2 `.ipynb` files with codes

## Explanations
### Setup File
The `establishments.json` file was uploaded into the `uk_food` database using `mongoimport`. Information for new establishment **Penang Flavours** was added to the collection by `insert_one()`. The `BusinessType` field was updated by checking the other documents in the collection and using `update_one()` to update the appropriate fields. 

Documents belonging to the Dover Local Authority was qeuried and deleted with `delete_many()`. `count_documents()` was used before and after deleting to make sure that the documents were deleted correctly.

Data types for latitude and longitude were changed from string to decimal using `$set...$toDouble`, and rating value was changed from string to integer with `$set...$toInt`. An aggregate function with `$project` was used to show the data types for the fields mentioned.

## Analysis File
To answer the first three questions, `find()` was used to find the documents with the necessary queries. After that, `json.normalize()` was used to turn the list to a DataFrame. For the final question, a aggregate pipeline was used to find the number of establishments with hygiene rating of 0 in each Local Authority.

## Credits
- Starter `.ipynb` files were given
