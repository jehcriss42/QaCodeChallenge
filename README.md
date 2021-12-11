## Challenge QA code

**1) About the API:**

  Api can be Downloaded and started as described in:
  https://bitbucket.org/adichallenge/products-docker-composer.git
  
**2) Project Test Cases**

It is used the API Testing Heuristics called VADER:

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
