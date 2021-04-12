# wk1_workshop

Objectives
Demonstrate your understanding of creating Node modules and implementing the Express router to route HTTP requests to different sets of endpoints, and respond to them. 


Instructions
In this assignment, you will complete the transition of the routing methods from Exercise: Express Router - Part 1 to the campsiteRouter in Part 2. You will also create and implement two more routers - one to handle promotions, and one to handle partners. You will be working with files in the node-express folder.



Task 1: Complete the updates to campsiteRouter
Update campsiteRouter.js (in node-express/routes) to include support for the /:campsiteId route parameter:


Add endpoints to campsiteRouter.js: Update campsiteRouter.js to include handling GET/POST/PUT/DELETE requests for /campsites/:campsiteId:

Add a new campsiteRouter.route() method, and as its argument, give it the path of '/:campsiteId'.

Chain an .all() method to the route() method you added above. Make it identical to the .all() method used for the existing campsiteRouter.route('/') method.

Chain .get(), .post(), .put(), and .delete() methods to this route as well. Refer back to the Express Router exercise, Part 1, to recall how these endpoints were handled, and handle them in the same way, updating the code to work with the router as you learned to do in Part 2 of that same exercise. 

Test: Use Postman to test each of your newly created endpoints and verify that you receive the expected responses. 
Test GET/POST/PUT/DELETE requests to: localhost:3000/campsites/1 
You do not have to use /1. You could just as well use /23, or /foo, or any other string in its place.
For the PUT request, make sure to send a JSON string in the body of the request with a name and description, the same way you did in the exercises. 


Task 2: Add an Express router to handle routing for promotions

Create a new router in a separate module to handle the endpoints for promotions:

Create promotionRouter: In the node-express/routes folder, create a Node module named promotionRouter.js that will implement the Express router for the following paths:

/promotions
/promotions/:promotionId
Endpoints: Write a route() method on the router for each of the paths above, just as you did with the campsiteRouter, chaining the .all(). .get(), .post(), .put(), and .delete() routing methods. Handle the responses in the same way as you did for the campsiteRouter.
Update server.js: Integrate the Node module you created above within your Express application code in server.js, in the same way as you did with the campsiteRouter.
Test: Use Postman to test each of your newly created endpoints and verify that you receive the expected responses. 
Test GET/POST/PUT/DELETE requests to: localhost:3000/promotions and localhost:3000/promotions/1
For the POST request to localhost:3000/promotions, make sure to send a JSON string in the body of the request with a name and description, the same way you did in the exercises. 
For the PUT request to localhost:3000/promotions/1, make sure to send a JSON string in the body of the request as you did for the POST request described above.


Task 3: Add an Express router to handle routing for partners

Create a new router in a separate module to handle the endpoints for partners:

Create partnerRouter: In the node-express/routes folder, create a Node module named partnerRouter.js that will implement the Express router for the following paths:

/partners
/partners/:partnerId
Endpoints: Write a route() method on the router for each of the paths above, just as you did with the campsiteRouter, chaining the .all(). .get(), .post(), .put(), and .delete() routing methods. Handle the responses in the same way as you did for the campsiteRouter.

Update server.js: Integrate the Node module you created above within your Express application code in server.js, in the same way as you did with the campsiteRouter.

Test: Use Postman to test each of your newly created endpoints and verify that you receive the expected responses.
Test GET/POST/PUT/DELETE requests to: localhost:3000/partners and localhost:3000/partners/1
For the POST request to localhost:3000/partners, make sure to send a JSON string in the body of the request with a name and description, the same way you did in the exercises. 
For the PUT request to localhost:3000/partners/1, make sure to send a JSON string in the body of the request as you did for the POST request described above.


Submission
Submit a zip file of your entire node-express folder with your updated files, excluding the node_modules folder, or submit a text file that contains the link to a public online Git repository for your project. 

Assignment Resources
Express - Router
Express - express.Router()
Express - Routing guide
