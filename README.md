## Challenge QA code

**1) About the API:**

  Api can be Downloaded and started as described in:
  https://bitbucket.org/adichallenge/products-docker-composer.git
  
**2) Project Test Cases**

It is used the API Testing Heuristics called VADER to create Test Cases and identify issues:

    Verbs
    Authorisation/Authentication
    Data
    Errors
    Responsiveness

**3) Tecnologies:**

    Postman/Newman
    javascript
    Docker/Jenkins
    

**4) Run the test:**

	 Instal docker-compose
	 Clone the following url: https://github.com/jehcriss42/QaCodeChallenge.git
	 Run docker-compose up
	 Access localhost:8080
	 On jenkins:
	 Run: Product

**OR**

	 Download the "Product.postman_collection.json" collection
	 Install newman and run:
	 newman run Product.postman_collection.json
	 

## Issues

1) There is no validation for id. It can be added more elements with same id what would cause inconsistency with the data.
2) Price Engine returns result for Products not registered in the Product database
3) Application has no Authorisation/Authentication
4) For Post a new product the Model indicates string but it accepts any type value and empty/null values
5) Internal Server Error (500) to Get a product id which do not exists in GET /product/{id} in Products
6) It is possible to Post empty body in POST /Product (GET and POST for /Product works in the same way)
7) It is possible to update empty body in PUT /Product (GET and PUT for /Product{id} works in the same way)
8) It is possibe to update a product which does not exist
9) Because it can be performed POST with empty values new items is registered which cannot be removed

### Consideration about Load Test

1) Because of the bugs with the endpoints load test could cause a huge inconsistency in the Database.
