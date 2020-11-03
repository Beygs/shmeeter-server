# Mini social network API

For educational purpose.

## Running Strapi

```shell
$ npm i
$ npm run develop
```

Then open [http://localhost:1337/admin](http://localhost:1337/admin) in a browser, and create an admin account.

Next, you can go in "Paramètres", and into "Rôles & Permissions", you can set up :

- For "Authenticated" role permissions:
  - for "Posts" (in "Application" section), check all action checkboxes.
  - for "User" (in "Users-Permissions" section), check "findone" and "me" checkboxes.
  - then, click "Save" button.
- For "Public" role permissions:
  - verify that for "Posts" there is no action checkbox checked, except for the "find" checkbox.
  - click "Save" button.

## Register

You can register a new user by doing a POST request on `http://localhost:1337/auth/local/register` with a JSON payload containing `username`, `email` and `password`.

## Login

You can login a user, by sending a POST request to `http://localhost:1337/auth/local` with a JSON payload containing `identifier` (with email or username) and `password`.

## Posts

You can create posts via `POST /posts` with JSON payload `{ "text": [post_message], "user": [creator_id] }`.

You can view all posts via `GET /posts`, and count them via `GET /posts/count`.

You can get one post via `GET /posts/[post_id]`.

You can delete a post via `DELETE /posts/[post_id]`.
