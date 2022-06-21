# THE RESTAURANT

## Intro
We have developed a mongoDB database for our Restaurant Client App. Now it is time to test that all the queries that the App will issue, are running correctly.

## Queries
We should issue the next queries:

1. Find the restaurant with id 30112340.
    db.Restaurants.find({restaurant_id: "30112340"}).pretty()  

2. Find May May Kitchen.
    db.Restaurants.find({name: "May May Kitchen"}).pretty()

3. Find the restaurants where their cuisine is Tapas.
    db.Restaurants.find({cuisine: "Tapas"}).pretty()

4. Find the restaurants in postal code 11208.
    db.Restaurants.find({'address.zipcode': "11208"})

5. Find all restaurants that have a score greater or equal than 70.
    db.Restaurants.find({'grades.score': {$gte: 70}}).pretty()

6. Find all restaurants in Brooklyn that have a score greater than 80
    db.Restaurants.find({$and: [{'grades.score': {$gt: 80}},{'borough': "Brooklyn"}]}).pretty()

7. All restaurants with Chilean or Czech cuisine.
    db.Restaurants.find({$or: [{cuisine: "Chilean"}, {cuisine: "Czech"}]}).pretty()

8. All restaurants with grade A in second position of the array.
    db.Restaurants.find({'grades.2.grade': "A"}).pretty()

9. All restaurants with grades A or B.
    db.Restaurants.find({grades: {$elemMatch: {$or: [{grade: "A"}, {grade: "B"}]}}}).pretty()

10. All restaurants that have a review made in 2014-09-16.
    db.Restaurants.find({grades: {$elemMatch: {'date': ISODate("2014-09-16T00:00:00Z")}}}).pretty()

11. All restaurant their cuisine is Tapas ordered by name in ascending (normal) order.
    db.Restaurants.find({cuisine: "Tapas"}).sort({"name": 1}).pretty()

12. How many restaurants have been graded after 2015-01-01.
    db.Restaurants.find({'grades.date': {$gte: ISODate("2015-01-01T00:00:00Z")}}).pretty()


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

