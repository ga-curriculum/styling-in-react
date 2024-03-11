# ![Styling in React - Styled Components](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to add style via an NPM package known as `styled-components`

## Styled components

Utilising [tagged template literals](https://wesbos.com/tagged-template-literals) (a recent addition to JavaScript) and the power of CSS, styled-components allow you to write actual CSS code to style your components. It also removes the mapping between components and styles. [source](https://styled-components.com/docs)

To use Styled Components we will need to install the package: [styled-components](https://www.npmjs.com/package/styled-components)

```bash
npm install styled-components
```

Next, we'll import the package at the top of the component as `styled`

```jsx
// src/components/example-4-styled-components/Button.jsx
import styled from 'styled-components'; // top of the component
```

After we have that imported, we will declare a variable that holds a styled button with our styles we want to apply to our component.  Note that we are using smart quotes so has to have these styles on multiple lines:

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