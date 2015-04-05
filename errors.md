# errors

A list of errors that the application can return.

```js
{
	errors: {
		BAD_FILE_TYPE: {
			description: 'The only valid file types are {{ validFileType }}. You uploaded a {{ uploadedFileType }} file.',
			status: 400
		},
		NO_FILE_UPLOADED: {
			description: 'The event handler requires a file to be passed in.',
			status: 400
		},
		FILE_TOO_LARGE: {
			description: 'The uploaded file was too large ({{ fileSize }} mb). It must be less than {{ maxFileSize }} mb.',
			status: 400
		}
	}
};
```