# ![Styling in React - tktk Microlesson Name](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to tktk

#### Example 2 : Inline CSS

<br>

About Inline Styling

Contrary to what we've been told about avoiding styling elements inline using the `style` attribute in HTML, with React, inline styling is a common technique for **dynamic** styling.

Inline styling in React uses the `style` property, however, unlike the `style` attribute in HTML, we assign a JS object instead of a string.

1. Create a `buttonStyle` variable and set it equal to an obj. Add your default button styles as key value pairs to this object. 

_Note:_ Unlike normal CSS, property key names will need to be camelCased and their values wrapped in a string. Dont forget your commas!

2. Set the `style` attribute in your component jsx equal to your `buttonStyle` object.


```jsx

export default function Button({ text }) {

  const buttonStyle = {
    // add styles here
  }

  return (
    <button style={buttonStyle}>{ text }</button>
  );
}
```




<br>
<br>

✨  Let's give it a fancy background-color: #b974b6

✨  Bonus: Let's change one of the style property values to a variable

✨  Bonus: Refactor your component to accept a props value that will set the style property in your css

<br>
<br>

#### Review Questions

**❓ What attribute do we use in JSX to apply css styles directly to components?**

**❓ What data type does the style attribute require?**

<br>
<br>
<br>
<br>
