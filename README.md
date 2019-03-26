## Getting Started

### Create Heroku app
1. Login to Heroku (if not already)
2. Click `New` -> `Create New App`
  + You can leave the defaults, or change them as needed
3. Click the `Create App` button

This app uses [`PostgreSQL`](https://www.postgresql.org/) as it's database, and Heroku has a free add-on you can use.

1. Click `Resources`
2. Under `Add-ons`, search for `postgres`
3. In the results drop down, click on  "Heroku Postgres"
4. Leave the selction as `Hobby Dev - Free`, then click the `Provision` button.
5 Copy the new application name for use later.

### Deploy this project
1. Preform steps above (Create Heroku app)
2. On your local machine in the root of the repo: `heroku login`
3. `heroku container:login`
4. `heroku container:push web --app "APP NAME HERE"` using the app name from step 5 in Create Heroku App
5. `heroku container:release web --app "APP NAME HERE"` using the app name from step 5 in Create Heroku App

Browse to https://app-name-here.heroku.com

If all went well you should get:

```json
  {
    "status": "Success",
    "message": "API is up and running",
    "code": 200
  }
```

And you should be able to browse to https://app-name-here.heroku.com/todos and perform API requests defined in this codepbase.

### Get Your Heroku API key
1. Click on your avatar in the upper right, then click `Account Settings`
2. Near the bottom, you will find `API key`. Click the `Reveal` button
3. Copy the API key
4. In the project files on your local machine, open `deployment.env.sample` and change `your_api_key_here` to your api key without any qutes.
13. Rename `deployment.env.sample` to `deployment.env`