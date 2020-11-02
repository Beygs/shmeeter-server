# Educational API for students

To test it, just run 

```shell
$ npm i
$ npm run develop
```

Then go on [http://localhost:1337/admin](http://localhost:1337/admin), create an admin account. Then, go on "Rôles et autorisations", and in "posts", check "find" and "findOne".


## Register & Login

You can register by going in POST on [http://localhost:1337/auth/local/register](http://localhost:1337/auth/local/register) then by sending in parameters a JSON object with `username`, `email`, `password`.

To login, send a POST to [http://localhost:1337/auth/local/](http://localhost:1337/auth/local/) with your credentials.



