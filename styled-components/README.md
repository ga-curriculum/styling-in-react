# ![Styling in React - Styled Components](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to add style via an NPM package known as `styled-components`

## Styled components

Styled components combine JavaScript's [tagged template literals](https://wesbos.com/tagged-template-literals) _(a recent addition to JS)_ with CSS, allowing you to write actual CSS for styling your components directly within your JavaScript files. This method simplifies the process by directly associating styles with components, eliminating the need for separate CSS files or class names. [_styled-components docs_](https://styled-components.com/docs)

To use Styled Components we will need to install the package: [styled-components](https://www.npmjs.com/package/styled-components)

```bash
npm install styled-components
```

Next, we'll import the package at the top of the component as `styled`

```jsx
// src/components/example-4-styled-components/Button.jsx

import styled from 'styled-components';
```

Define a styled component using the `styled` function. For example, to create a styled button, declare a `StyledButton` variable and use backticks `` ` `` to write your CSS:

```jsx
// src/components/example-4-styled-components/Button.jsx

const Button = ({ text }) => {

  const StyledButton = styled.button`
    background-color: #86ba8a;
    border-radius: 8px;
    color: #3d3d3d;
    padding: 15px 50px;
    font-size: 24pt;
    width: 300px;
  `;
```

In this approach, the `StyledButton` variable is a React component with your specified styles applied. You can use this component in your JSX just like any other React component.


Lastly, we will take that variable and render it as a component:

```jsx
  return (
    <StyledButton>{ text }</StyledButton>
  );
};
```

The full styled component looks like this:

```jsx
// src/components/example-4-styled-components/Button.jsx
import styled from 'styled-components';

const StyledButton = styled.button`
  background-color: #86ba8a;
  border-radius: 8px;
  color: #3d3d3d;
  padding: 15px 50px;
  font-size: 24pt;
  width: 300px;
`;

const Button({ buttonText }) => {
  return <StyledButton>{buttonText}</StyledButton>;
};

export default Button;
```

You got it!

## Benefits and pitfalls

Using styled-components, styles are tightly coupled with components, leading to more modular and reusable code. This method promotes the creation of self-contained components where both logic and style are defined together, enhancing code clarity and ease of maintenance. As far as libraries go, this one is among the most popular. 

For developers new to this approach, there can be a learning curve in understanding how to use JavaScript for styling. This method also potentially increases the complexity of the code, as it blends CSS with JavaScript, which might not be preferable for those who like to keep styling separate from scripting.