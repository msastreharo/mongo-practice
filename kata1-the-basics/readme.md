# THE RESTAURANT

## Intro
We have developed a mongoDB database for our Restaurant Client App. Now it is time to test that all the queries that the App will issue, are running correctly.

## Queries
We should issue the next queries:

1. Find the restaurant with id 30112340.
2. Find May May Kitchen.
3. Find the restaurants where their cuisine is Tapas.
4. Find the restaurants in postal code 11208.
5. Find all restaurants that have a score greater or equal than 70.
6. Find all restaurants in Brooklynthat have a score greater than 80
7. All restaurants with Chilean or Czech cuisine.
8. All restaurants with grade A in second position of the array.
9. All restaurants with grades A or B.
10. All restaurants that have a review made in 2014-09-16.
11. All restaurant their cuisine is Tapas ordered by name in ascending (normal) order.
12. How many restaurants have been graded after 2015-01-01.

### Steps

To prepare the test environment:
1. Fork this repository
2. Clon your forked repository to local
3. Open a terminal pointing to the cloned folder and run the next command:

```bash
mongoimport --db restaurants --collection restaurants --file primer-dataset.json
```
To run the tests:

4. Open the mongo shell (mongo terminal client) with the `mongo` command
5. Run the queries to solve the exercise
6. Copy all the queries into the readme.md document.
7. Push changes to your forked repositories.
8. Issue a pull-request to the original kata repository with your name.

