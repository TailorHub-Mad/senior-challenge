# Tailor

## The Challenge

The task is to write a restaurants application in TypeScript. 
Attached below are a series of steps you can take for guidance progressively.

## Backend

We have a simple SQLite database with some tables.
Create a an API with the following endpoints:
At Tailor, we use TypeScript, Express and NestJS for our projects, but feel free to use any other framework you are comfortable with.

### Public endpoints:
	1.	GET /restaurants:
	•	Pagination: page, limit.
	•	Filters: cuisine, rating, neighborhood.
	•	Sorting: sort (ascendente/descendente por campo).
	2.	GET /restaurants/:id
	3.	GET /restaurants/:id/reviews
	4.	POST /auth/login
	5.	POST /auth/register

### Authenticated endpoints (roles: USER or ADMIN):
	6.	GET /me: Information about the authenticated user.
	7.	GET /me/reviews: Reviews created by the authenticated user.
	8.	POST /restaurants/:id/reviews: Create a review.
	9.	PUT /me/reviews/:id: Edit a review.
	10.	DELETE /me/reviews/:id: Delete a review.
	11.	POST /me/favorites/:restaurantId: Add a restaurant to favorites.
	12.	DELETE /me/favorites/:restaurantId: Delete a restaurant from favorites.
	13.	GET /me/favorites: See the list of favorites.

### Admin endpoints:
	14.	POST /restaurants: Create a restaurant.
	15.	PUT /restaurants/:id: Edit a restaurant.
	16.	DELETE /restaurants/:id: Delete a restaurant.
	17.	GET /admin/stats: See statistics (e.g., number of users, reviews, restaurants).

### Middlewares    

[ ] Middleware for authentication
[ ] Middleware for roles

### Scalability

As a second step, imagine that your application is growing over time. Scalability is key.
You will need to think of some strategies to make your application scalable. 

Some pointers or ideas:

[ ] Rate Limiting
[ ] Caching
[ ] Docker

### Architecture diagram

Please use draw.io, excalidraw or any similar schema tools to create a diagram of the overall architecture of your application.

[ ] Diagram 1: expose to us how you have designed your current application.

Imagine that after some time our application has *100.000 users per week* and some peak timings during the day with a lot of requests & traffic. 

[ ] Diagram 2: expose to us how you would scale your application with these new conditions and what you would do to improve the performance of your application.


## Frontend

Create an app that displays the restaurants from your API. You can use any framework you want.
Most projects from Tailor are built with Next.js (React) or Nuxt.js (Vue).
Bonus points if you use those, but it's not mandatory.

### Requirements

[ ] Use a state management system to persist the state of the app.
[ ] Display an initial list with all restaurants.
[ ] When a restaurant is selected from the list, it will render a restaurant detail view displaying a few more details about that restaurant
[ ] Enable CRUD actions for restaurants, and develop the corresponding pages.
[ ] Enable CRUD actions for comments.
[ ] Display a spinner or placeholder component while the API request is ongoing.
[ ] Make it look visually appealing. Reproduce the figma design as accurate as possible, but it does not necessarily have to be perfect. Add images for each device.

Push the code to a public github repository with a README.md that explains how to run API & Frontend apps.
Then, email it to us.

## Design

Figma link: https://www.figma.com/file/LuwjRZZb3ms0MeAmu7gZch/Tailor-Prueba-t%C3%A9cnica-Junior?type=design&node-id=2%3A15&mode=design&t=mYbsPNUJscBcb7yN-1

## Bonus points

1. Deploy the app.
2. Write realistic unit & end-to-end tests.
3. Good documentation is appreciated (with tools like Swagger, Postman, etc or just explicit guidance in the README.md)