# React Bootstrap Notifier

> A react component to show growl-like notifications using [bootstrap alerts](http://getbootstrap.com/components/#alerts).

See a [live demo](https://chadly.github.io/react-bs-notifier/).

## Usage

```
npm install react-bs-notifier --save
```

To show a list of different types of alerts in the top right corner of the page:

```js
import React from "react";
import ReactDOM from "react-dom";
import { AlertList } from "react-bs-notifier";

const alerts = [{
	id: 1,
	type: "info",
	message: "Hello, world"
}, {
	id: 2,
	type: "success",
	message: "Oh, hai"
}]

ReactDOM.render((
	<AlertList alerts={alerts} />
), document.getElementById("myApp"));
```

Or to show a single inline-alert:

```js
import React from "react";
import ReactDOM from "react-dom";
import { Alert } from "react-bs-notifier";

ReactDOM.render((
	<Alert type="danger" headline="Error!">
		Holy cow, man!
	</Alert>
), document.getElementById("myApp"));
```

Or show alerts without creating an array (equivalent to first example):

```js
import React from "react";
import ReactDOM from "react-dom";
import { Alert, AlertContainer } from "react-bs-notifier";

ReactDOM.render((
	<AlertContainer>
		<Alert type="info">Hello, world</Alert>
		<Alert type="success">Oh, hai</Alert>
	</AlertContainer>
), document.getElementById("myApp"));
```

[Read the documentation](https://chadly.github.io/react-bs-notifier/) for more in-depth, interactive examples and live demos.

## Contributing

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

If you have a new feature or change you'd like to submit, please make sure to also update the documentation. Once you clone this repo, you can run the docs & example app locally:

```
npm install
npm start
```

This will spin up a webpack dev server on port 1341. Open your browser to [localhost:1341](http://localhost:1341/) and any changes you make will build & refresh the page automatically.

### Deploying Docs to Github Pages

This is mostly a note for me so I don't forget. Run `npm run build --production` and commit the resulting `example/index.html` & `example/build.js.*` files to the `gh-pages` branch.