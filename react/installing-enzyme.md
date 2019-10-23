# Installing Enzyme

## What is Enzyme?

Enzyme is a JavaScript Testing utility for React that makes it easier to test your React Components' output. You can also manipulate, traverse, and in some ways simulate runtime given the output.

## Installation

You will need to install enzyme along with an Adapter corresponding to the version of react (or other UI Component library) you are using. If you are using enzyme with React 16, you can run:

`npm i --save-dev enzyme enzyme-adapter-react-16`

Check [here](https://airbnb.io/enzyme/) to find the right adapter for your React version.

## Configure

Finally, you need to configure enzyme to use the adapter you want it to use.

Create a `setupTests.js` file in the root of the project. Add the following to the file:

```js
import { configure } from 'enzyme';
import Adapter from 'enzyme-adapter-react-16';

configure({ adapter: new Adapter() });

const localStorageMock = {
  getItem: jest.fn(),
  setItem: jest.fn(),
  removeItem: jest.fn(),
  clear: jest.fn()
};
global.localStorage = localStorageMock;
```

## Types of rendering

### Render

Generates HTML from the react tree. We can then analyze this HTML

### Shallow

Useful for unit testing components.

### Mount

This renders the full DOM. Useful for testing components that are wrapped in higher order components or interact with DOM APIs e.g. fetch

[Main Page](../README.md)
