
# heroku-deno-getting-started

## Buildpack

https://github.com/chibat/heroku-buildpack-deno

## Running Locally
Make sure you have [Deno](https://deno.land/) and the [Heroku CLI](https://cli.heroku.com/) installed.
```
$ git clone https://github.com/chibat/heroku-deno-getting-started.git
$ cd heroku-deno-getting-started
$ deno run --allow-net=:8080 --config tsconfig.json --unstable --importmap import_map.json app.ts --port=8080
```
Your app should now be running on [localhost:8080](http://localhost:8080/).

## Deploying to Heroku
```
$ heroku create --buildpack https://github.com/chibat/heroku-buildpack-deno.git
$ git push heroku master
$ heroku open
```

