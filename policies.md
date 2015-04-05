# policies

A list of policies that can be run before specific event handlers.

```js
{
	policies: {
		isLoggedIn: function(req, res, cb) {
			if(!req.session.user) {
				return cb(/* get unauthorized error*/);
			}
			cb();
		}
	}
};
```