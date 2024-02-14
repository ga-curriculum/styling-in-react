# ![Styling in React - tktk Microlesson Name](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to tktk

#### Example 4 : Styled Components

<br>

To use Styled Components we will need to install the package: [styled-components](https://www.npmjs.com/package/styled-components)

`npm install styled-components`

Utilising [tagged template literals](https://wesbos.com/tagged-template-literals) (a recent addition to JavaScript) and the power of CSS, styled-components allows you to write actual CSS code to style your components. It also removes the mapping between components and styles. [source](https://styled-components.com/docs)

```jsx
import styled from "styled-components";

export default function Button({ text }) {
  
  const StyledButton = styled.button`
    add styles here using css syntax
  `;

  return (
    <StyledButton>{ text }</StyledButton>
  );
}
```

<br>
<br>

✨  Let's give it a fancy background-color: #86ba8a  &  text color: #3d3d3d

✨  Bonus: refector to accept props and add a prop style

<br>
<br>

#### Review Questions

**❓ What syntax is used inside the tagged template literal?**

**❓ What is one benefit of using styled components?**

<br>
<br>
<br>
<br>

