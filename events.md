# events

Events are the core foundation of each component. Events are triggered by user (or other) actions and then are handled in the proper (asynchronous) order by the functions listed for that event.

```js
{
	events: {
		login_attempt: {
			description: 'Triggered when a user tries to log in to the app.',
			handlers: {
				validation: {
					type: 'front',
					dependencies: [],
					policies: [],
					run: function(e, cb) {
						// Still unsure on the params that get passed to
						// these run functions. Ideally I'd like them to
						// be consistent between front and back.
					}
				},
				authentication: {
					type: 'back',
					dependencies: ['validation'],
					policies: [], // policies to run before the handler is run
					run: function(req, res, models) {
						// Still unsure on the params that get passed to
						// these run functions. Ideally I'd like them to
						// be consistent between front and back.
					}
				}
			},
			success: function(results) {
				// Called if all of the handlers successfully run
			},
			error: function(err) {
				// Called if an error is thrown in any of the handlers
			}
		},
		forgot_password_click: {
			description: 'Triggered when a clicks on the forgot password link.',
			handlers: {
				// ...
			}
		}
	}
};
```