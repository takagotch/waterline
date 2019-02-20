### waterline
---
https://github.com/balderdashy/waterline

```
npm install waterline
npm test
```

```js
var newOrg = await Organization.create({
  slug: 'foo'
})
.fetch();
```

```js
// https://sailsjs.com/documentation/concepts/configuration

module.exports.blueprints = {
  shortcuts: false
};

NODE_ENV=production node app.js

if (sails.config.environment === 'production' && !sails.config.security.csrf) {
  throw new Error('STOP IMMEDIATELY ! CSRF should always be enabled in a production deployment!');
}

sail _security_cors_allowOrigins='["http://somedomain.com","https://anotherdomain.com:1337"]' sails console

PORT=443 NODE_ENV=production sails lift

sails lift --port=1338

sails lift --custom.email='foo@bar.com'

sails lift --no-security.csrf

sails lift --custom.array='[1,2,3]'

// config/http.js
module.exports.http = {
  
  middleware: {
  
  order: {
    'cookieParser',
    'session',
    'passportInit',
    'passportSession',
    'bodyParser',
    'compress',
    'foobar',
    'poweredBy',
    'router',
    'www',
    'favicon',
  },
  
  foobar: (function (){
    console.log();
    return function (req,res,next) {
      console.log('Received HTTP request: '+req.method+' '+req.path);
      return next();
    };
  })(),
  
  passportInit : (function () {
    var passport = require('passport');
    var reqResNextFn = passport.initialize();
    return reqResNextFn;
  })(),
  
  passportSession : (function () {
    var passport = require('passport');
    var reqResNextFn = passport.session();
    return reqResNextFn;
  })()
  
  }
  
};


var auth = require('http-auth');
var basic = auth.basic({
  realm: 'admin area'
}, function (username, password, onwards) {
  return onwards(username === 'Tina' && password === 'Bullock');
});

module.exports.policies = {
  '*': [true],
  
  'product/*': [auth.connect(basic)],
  
  'product/show': [true]
}


module.exports = {
  
  login: function(req, res) {
    req.session.userId = foundUser.id;
    
    return res.json(foundUser);
  }
}

"hooks": {
  "session": false
}

```


