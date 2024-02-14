# ![Styling in React - tktk Microlesson Name](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to tktk

#### Example 3 : CSS in JS

<br>

To use CSS in JS we will need to install the package: [react-jss](https://cssinjs.org/react-jss/?v=v10.9.0).

`npm install react-jss `

This library also uses javascript objects to describe styles in a declarative way. Its custom method ‘createUseStyles’ then incorporates those styles into functional components using the JSX className attribute.

```jsx
import { createUseStyles } from "react-jss";

export default function Button({ text }) {

  const styles = createUseStyles({
    button: {
      // add your styles as JS key : value pairs
    }
  });

  const classes = styles()

  return (
    <button className={ classes.button }>{ text }</button>
  );
}
```

<br>
<br>

✨  Let's give it a fancy background-color: #24292e  &  text color: #f7df1c

✨  Bonus: refector to accept props and add a prop style

<br>
<br>

#### Review Questions

**❓ What method does react-jss use to apply style objects?**

**❓ What jsx attribute is used to apply the style object created by react-jss?**

<br>
<br>
<br>
<br>

