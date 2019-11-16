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

## Step Four - Use Rails Console to Create a User

We removed the routes to create a User because we only want developers to be able to do that. The way our developers will create new users for this app is to use the rails console. Use the rails console to create 2 users. Paste the commands you used into the `SOLUTIONS.md` file.

> > first_user = User.create
> > (0.1ms) begin transaction
> > User Create (0.4ms) INSERT INTO "users" ("created_at", "updated_at") VALUES (?, ?) [["created_at", "2019-11-16 21:55:38.439787"], ["updated_at", "2019-11-16 21:55:38.439787"]](1.0ms) commit transaction
> > => #<User id: 1, email: nil, active: nil, created_at: "2019-11-16 21:55:38", updated_at: "2019-11-16 21:55:38">
> > second_user = User.create
> > (0.1ms) begin transaction
> > User Create (0.7ms) INSERT INTO "users" ("created_at", "updated_at") VALUES (?, ?) [["created_at", "2019-11-16 21:55:51.651067"], ["updated_at", "2019-11-16 21:55:51.651067"]](0.6ms) commit transaction
> > => #<User id: 2, email: nil, active: nil, created_at: "2019-11-16 21:55:51", updated_at: "2019-11-16 21:55:51">
