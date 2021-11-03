#  Interaction of two APIs React-Rails, Frontend-Backend #
Works together with [Rails API]( https://github.com/HarshBarash/Rails_API_wReact_API )


#  Clone the repository, run #

```javascript
$ npm run start
```

## Navigate to http://localhost:3000/: ##

# Set up the App* #
(If you create it yourself)

```javascript

$ npx create-react-app frontend-api

$ cd frontend-api/

$ yarn add http-proxy-middleware

```

## In /src, create a file called setupProxy.js ##

```javascript

const { createProxyMiddleware } = require('http-proxy-middleware');
module.exports = function(app) {
    app.use(
        '/api',
        createProxyMiddleware({
            target: 'http://localhost:3001',
            changeOrigin: true,
        })
    );
};

```

```javascript

npm run start

```

## Navigate to http://localhost:3000/: ##


*Don't forget to follow the instructions for the [Rails API]( https://github.com/HarshBarash/Rails_API_wReact_API ) as well

*If you have similar "create-react-app is not working since version 4.0.1" problems, follow the instructions


Uninstall create-react-app v4.0.1:

1. 
```javascript

# for npm:
npm uninstall -g create-react-app

# for yarn:
yarn global remove create-react-app

```

2. 
```javascript

# for npm:
npm i create-react-app

# for yarn:
yarn add create-react-app

```

3.
```javascript

# for npx:
npx create-react-app my-app

# for npm:
npm init react-app my-app

# for yarn:
yarn create react-app my-app

```

*If it didn't solve the [ problem ]( https://stackoverflow.com/questions/64963796/create-react-app-is-not-working-since-version-4-0-1 )


