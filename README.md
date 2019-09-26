# brrs-two-heroku

## Overview:

This app runs on Heroku (though just barely) and it runs locally.

This app has all fonts and the dev build removed and almost all components removed. It also has a lot of code commented out which otherwise would not be (for instance `workbox-webpack-plugin` and other plugins in 'prod.client.js').

You might notice I add comments to code. I figured I would include some for context. 

I'm not good at naming apps so it's just called "brrs-two-heroku".

This app is a total work in progress.

It might be running here:

* [https://webpack-scss-react-redux-demo.herokuapp.com/](https://webpack-scss-react-redux-demo.herokuapp.com/)

## Installation On Heroku:

1. Uncomment line 8 `require('./start');` in 'bin/server.js'
2. Comment line 9 `require('./localStart')` in 'bin/server.js'
3. `git init`
4. `git add .`
5. `git commit -m "Initial commit."`
6. `heroku login`
7. `heroku create`
8. `heroku config:set YARN_PRODUCTION=false`
9. `git push heroku master`

## Installation Local:

1. Uncomment line 9 `require('./localStart')` in 'bin/server.js'
2. Comment line 8 `require('./start');` in 'bin/server.js'
3. `yarn start`
4. `localhost:8080`

### FYI: Not sure if Node CLI `NODE_OPTIONS=--max-old-space-size` works in start script. Not sure if has any affect on Heroku.

* [https://nodejs.org/api/cli.html](https://nodejs.org/api/cli.html)