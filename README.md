# react-app-heroku-environemnt-buildpack

Build pack to let heroku environment variables through as react app variables


### USAGE

1. Define a HEROKU_TO_REACT_APP_VARIABLES env variable in your heroku app. It should mention all the variables that need to be whitelisted. e.g

```
HEROKU_TO_REACT_APP_VARIABLES=HEROKU_SLUG_COMMIT, HEROKU_VAR_2, HEROKU_VAR_3
```

2. Add this buildpack before create-react-app buildpack

3. Your environment variables will be renamed and available with `REACT_APP_` prefix. The above variables will rename as,

```
HEROKU_SLUG_COMMIT => REACT_APP_HEROKU_SLUG_COMMIT
HEROKU_VAR_2 => REACT_APP_HEROKU_VAR_2
HEROKU_VAR_3 => REACT_APP_HEROKU_VAR_3
```
