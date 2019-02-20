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
```


