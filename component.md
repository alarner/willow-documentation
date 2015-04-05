# component

A component is a self-contained set of code that accomplishes a single task. This particular component is responsible for uploading a file to the server. All components have a render method that builds the user interface for the component. Components can be made of other components.

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