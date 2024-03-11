# ![Styling in React - Imported CSS Files](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able add style via imported CSS files in their React app.

## Implementing external stylesheets

Let's see how to implement External CSS stylesheets in React app.

To begin, import `Button1` into `src/App.jsx`:

```jsx
// src/App.jsx
import './App.css';
import Button1 from './components/example-1-normal-css/Button';
.
.
.
function App() {
  return (
    <div className='App'>
      <Button1 buttonText='Example 1' />
    </div>
  );
};
```

Next, create a style sheet inside the `example-1-normal-css` directory:

```bash
touch src/components/example-1-normal-css/button.css
```

After creating the file, we can import it into `src/components/example-1-normal-css/Button.jsx` like so:

```jsx
// src/components/example-1-normal-css/Button.jsx
import './button.css';
```

Next we'll add a `btn` class to our `<button>` tag using the JSX attribute `className`:

```jsx
// src/components/example-1-normal-css/Button.jsx
import './button.css';

const Button = ({ buttonText }) => {
  return (
    <button className='btn'>{ buttonText }</button>
  );
};

export default Button;
```

All the remains is to add some styling to `src/components/example-1-normal-css/button.css`:

```css
/* src/components/example-1-normal-css/button.css */
.btn {
  background-color: #2465f1;
  border-radius: 8px;
  color: white;
  font-size: 24pt;
  padding: 15px 50px;
  width: 300px;
}
```