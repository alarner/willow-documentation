# options

Metadata describing the options that should be passed in to this component.

```js
{
	options: {
		theme: {
			description: 'A string representing the theme to use for this component.',
			type: 'string',
			required: true,
			defaultsTo: 'bootstrap',
			validations: function(val) {
				// Return an object with original and formatted value on success.
				return: {
					original: val,
					formatted: val.trim()
				};
				// else return a descriptive error object if val is invalid.
			}
		}
	}
};
```