```js
import errors from './errors';
import events from './events';
import models from './models';
export default {
	description: 'A component that handles uploading and storing a file.',
	route: null,
	errors: errors,
	events: events,
	models: models,
	render: function() {
		return (
			<input type="file" ref="uploadButton" />
		);
	}
}
```