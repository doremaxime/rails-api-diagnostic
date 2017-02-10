# Rails API Diagnostic

Place your responses inside the fenced code-blocks where indicated by comments.

What is the purpose of a backend?

```md
For a website to connect to the web which allows users to interact throught a site.
```

Which layer in the MVC pattern is used by the controller to fetch data?

```md
I am not sure what is meant by 'layer'. the controller sends the information it got from the server to the model so that information from the database is sent back.
```

Which layer in the MVC pattern communicates with the model?

```md
I am not sure what is meant by 'layer'. The model gets a request from the controller to fetch data from the database by converting the ruby into sql and sends the data back to the controller.
```

Why don't we use views in our interpretation of the MVC pattern?

```md
Not sure, I was asking myself that the other day. We have just been using the controller to send json to the user instead of making it available to the views. I thought the views is what the user saw, but they can also see it with json?
```

What does C.R.U.D stand for?

```md
create, read, update, delete
```

In which part of the MVC pattern can we find C.R.U.D actions?

```md
The controller.
```

List at least 5 standard rails actions that C.R.U.D requests correspond to?

```md
index, show, new, create, edit, update, destroy.
```

A user action fires a `GET` request for `/people/1`. Explain in detail each step
required for data to be returned to the client. (bullet points or ordered list)

```md
-The router recieves the request and routes it to the correct controller sending along the parameters.
-Controller's show action reeives te request and send (in ruby) a message to get the the ID1 of people.
-the model uses activerecords to convert ruby into SQL.
-The SQL retrieves the required data from the database and sends it back throught the model to the controller.
-The controller makes the data availabl to the views.
-The views turn the data into relevant layout, putting it all on one static page and sends it back to the controller.
-The controller that back to the user.
-The user's browser renders the final page to the user.
-The user sees it says 'ok, I really don't need to post this person's profile because I feel like a creep..'
```

What is the command to generate a new rails-api app?

```bash
touch scripts/examples/index.sh
```

What is the command to start an instance of a rails server?

```bash
bin/rails server
```

What are the commands to drop, create, migrate and seed a database from the command
line? (5 bullet points)

```bash
bin/rake db:create
bin/rake db:migrate
bin/rake db:drop
bin/rake db:seed
```

What is the command to scaffold a pet with a name and age attributes (hint:
Also think of the data types for each attribute)?

```bash
bin/rails generate scaffold post name:string age:integer
or
bin/rails generate scaffold post pet_name:string pet_age:integer
depending on the table(s) name(s) and what not.

```
