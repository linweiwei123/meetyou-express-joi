# joi express middleware

npm install meetyou-express-joi --save

# github
https://github.com/linweiwei123/meetyou-express-joi

# Example

```javascript
const ExpressJoi = require('meetyou-express-joi');

const bodySchema = {
  query: {
    name: Joi.string().max(20).required(),
    company: Joi.string().max(60).required(),
    position: Joi.string().max(60).required(),
    phone: Joi.string().length(11).required(),
    email: Joi.string().email().max(50).required()
  }
};

 app.get('/brand_invitation/save', ExpressJoi(bodySchema), (req, res, next) => {
 })
 ```

