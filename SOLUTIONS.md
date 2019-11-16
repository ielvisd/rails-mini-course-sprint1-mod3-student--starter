1. What controller and action handles the data from the form submission?

   - The controller that handles the data from the form submission is: `tasks_controller.rb`.
   - The action is `create`.

2. What controller and action would be used if you did a `GET` request on the `/users` route?

   - The controller used would be: `users_controller.rb`.
   - The action is `index`.

3. Write out the step-by-step process that your rails application will take to render the `tasks/new` route.

   1. The browser issues a request for the `tasks/new` URL.
   2. Rails routes /users to the `new` action in the Tasks controller.
   3. The `new` action asks the Tasks model to create a new task (`Task.new`) with the provided
   4. The `Task` model pulls the Task structure from the database.
   5. The `Task` model returns the task structure to the controller.
   6. The controller captures the task in the `@task` variable, which is passed to the `new` view.
   7. The view uses embedded Ruby (.erb) to render the page as HTML.
   8. The controller passes the HTML back to the browser.

4. What file is responsible for managing the mapping between your application and the `tasks` database table?

   - `task.rb` ?

5. Explain all 7 of the RESTful actions in Rails

   - List each action by its name
   - Explain which HTTP verbs pair with each action
   - Write a short sentence for each action that summarizes what it does

Example for `users`:
HTTP Verb Path Controller#Action Used for

- GET /users sers#index display a list of all photos
- GET /users/new users#new return an HTML form for creating a new user
- POST /users users#create create a new user
- GET /users/:id users#show display a specific user
- GET /users/:id/edit users#edit return an HTML form for editing a user
- PATCH/PUT /users/:id users#update update a specific user
- DELETE /users/:id users#destroy delete a specific user
