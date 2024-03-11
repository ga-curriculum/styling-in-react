# ![Styling in React - CSS in JavaScript](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to style their React components with CSS in JavaScript.

## Implementing CSS in JavaScript

To use CSS in JS we will need to install the package: [react-jss](https://cssinjs.org/react-jss/?v=v10.10.0).

To describe our styles we make use of a custom method called `createUseStyles`. The `createUseStyles` method is passed an object. Each key in this object corresponds to a class name, and its value is another object containing CSS properties and values. When applying the styling, these class names can be accessed through dot notation. Let's try it out!

First we will need to install the package:

```bash
npm install react-jss
```

Next, we will import the `createUseStyles` method at the top of our component:

```jsx
// src/components/example-3-css-in-js/Button.jsx
import { createUseStyles } from 'react-jss';
```

Once we have the `createUseStyles` method imported, we will pass an object into the method with a key of `btn`. The key of `btn` will be assigned an object that will hold the CSS styles we want to apply to our button. We store this configuration into a variable called `styles` which we will call and store within `classes`:

```jsx
// src/components/example-3-css-in-js/Button.jsx
const Button = ({ buttonText }) => {

  const styles = createUseStyles({
    btn: {
      backgroundColor: '#24292e', // adding the styles in the object that we'll apply to our button
      borderRadius: '8px',
      color: '#f7df1c',
      fontSize: '24pt',
      padding: '15px 50px',
      width: '300px',
    },
  });

  const classes = styles();
```

When we want to apply `styles` to the button, we pass the value of `classes.btn` as the value for the attribute `className` in our `button` element:

```jsx
// src/components/example-3-css-in-js/Button.jsx
  return (
    <button className={classes.btn}>
      {buttonText}
    </button>
  );
};

export default Button;
```

The entire component will look like this when you have added all of your code:

```jsx
// src/components/example-3-css-in-js/Button.jsx
import { createUseStyles } from 'react-jss';

const Button = ({ buttonText }) => {

  const styles = createUseStyles({
    btn: {
      backgroundColor: '#24292e', // adding the styles in the object that we'll apply to our button
      borderRadius: '8px',
      color: '#f7df1c',
      fontSize: '24pt',
      padding: '15px 50px',
      width: '300px' d,
    },
  });

  const classes = styles(); // calling styles and storing it in classes

  return (
    <button className={classes.btn}>
      {buttonText}
    </button> // using the btn key from the classes variable to grab the stored styles
  );
};

export default Button;
```