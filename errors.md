# errors

 A list of errors that the application can return

```js
{
	errors: {
		BAD_USERNAME: {
			description: 'The username {{username}} is invalid.',
			status: 400
		},
		MISSING_USERNAME: {
			description: 'You must specify a username before logging in.',
			status: 400
		}
	}
};
```