# ![Styling in React - Imported CSS Files](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able add style via imported CSS files in their React app.

## Bringing our button component into `App.jsx`

`App.jsx`:
```jsx
import './App.css';
import Button1 from './components/example-1-normal-css/Button'
.
.
.
function App() {
  return (
    <div className='App'>
      <Button1 buttonText='Example 1' />
    </div>
  )
}
```

### Create a css style sheet in our component folder

```bash
touch src/components/example-1-normal-css/button.css
```

### Import the css file into your component file

`src/components/example-1-normal-css/Button.jsx`:
```jsx
import './button.css'
```
### Add classes in JSX using the JSX attribute `className`

```jsx
import './button.css';

const Button = ({ buttonText }) => {
  return (
    <button className='btn'>{ buttonText }</button>
  )
}

export default Button
```

### Add style to our `button.css` file:

`src/components/example-1-normal-css/button.css`:
```css
.btn {
  background-color: #2465f1;
  border-radius: 8px;
  color: white;
  font-size: 24pt;
  padding: 15px 50px;
  width: 300px;
}
```