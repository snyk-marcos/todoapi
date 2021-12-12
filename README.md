<h3 align="center">
    TodoAPI: A simple API to manage tasks
</h3>

<p align="center">
  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/marcosbergami/todoapi">

  <a href="https://www.linkedin.com/in/marcos-bergami-160771112">
    <img alt="Made by Marcos Bergami" src="https://img.shields.io/badge/made%20by-Marcos%20Bergami-blueviolet">
  </a>

  <img alt="Last commit" src="https://img.shields.io/github/last-commit/marcosbergami/todoapi">
</p>

## :bookmark_tabs: TodoAPI

I am a current student of the Ignite program presented by **[Rocketseat](https://www.rocketseat.com.br/)**.

Within every module, the course offers main challenges and extra assignments you can complete to enhance your skills and have fun.

This challenge consisted of us creating an API that is capable of adding users to the platform as well as allowing the users themselves to create, update, and remove tasks on their profile.

### Application routes

The back-end of this newly created API, has a total of 6 routes at the moment.

- **`POST /users`**: This route receives the properties `name` and `username` inside of the request body. A middleware handles a validation to check if a user already exists based on the properties received. If all validations pass, a new user is created in the following format: `{ id: 'uuid', name: 'John Doe', username: 'johndoe', todos: [] }`

- **`GET /todos`**: This route will receive the property `username` inside of the request header and return all of the todos associated with that specific user.

- **`POST /todos`**: This route will receive the propeties `title` and `deadline` inside of the request body, as well as the property `username` inside of the request header. The new *todo* will be associated with the user found based on the properties received.

- **`PUT /todos/:id`**: This route will receive the property `username` inside of the request header, and the properties `title` and `deadline` inside of the request body. The task associated with the `id` passed as a route param, will have its title and deadline updated.

- **`PATCH /todos/:id/done`**: This route will receive the property `username` inside of the request header. The task associated with the received username and id will have its status altered to **done**.

- **`DELETE /todos/:id`**: This route will receive the property `username` inside of the request header, and delete the *todo* associated with the username and id received.

This was an overall fun challenge to complete. It made me practice a few array methods and middleware creation.

---

Made with :heart: by Marcos Bergami