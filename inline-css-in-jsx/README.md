# ![Styling in React - Inline CSS in JSX](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to apply style to their React components using inline CSS in JSX.

## About Inline Styling

Contrary to what we've been told about avoiding styling elements inline using the `style` attribute in HTML, with React, inline styling is a common technique for **dynamic** styling.

Inline styling in React uses the `style` property, however, unlike the `style` attribute in HTML, we assign a JS object instead of a string.

### Applying Inline Style

In `src/components/example-2-inline-css/Button.jsx`, create a `buttonStyle` variable and set it equal to an object. Add your default button styles as key value pairs to this object.

`Button.jsx`:
```jsx
const buttonStyle = {
  backgroundColor: '#b974b6',
  borderRadius: '8px',
  color: 'white',
  fontSize: '24pt',
  padding: '15px 50px',
  width: '300px',
};
```

_Note:_ Unlike normal CSS, property key names will need to be camelCased and their values wrapped in a string. Dont forget your commas!

Set the `style` attribute in your component jsx equal to your `buttonStyle` object.

`Button.jsx`:
```jsx

const Button = ({ text }) => {

  const buttonStyle = {
    backgroundColor: '#b974b6',
    borderRadius: '8px',
    color: 'white',
    fontSize: '24pt',
    padding: '15px 50px',
    width: '300px',
  };

  return (
    <button style={buttonStyle}>{ text }</button>
  );
}

export default Button
```