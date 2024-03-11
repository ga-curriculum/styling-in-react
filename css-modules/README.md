# ![Styling in React - CSS Modules](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to add style to React components using CSS Modules.

## CSS Modules

With **CSS Modules**, a CSS file's **class names** will be made unique by the tooling and will be dedicated to the component that imports the CSS Module. 

Using a CSS Module differs from using a CSS stylesheet in three ways:

1. The filename ends with `module.css`, e.g., `button.module.css` instead of `button.css`.
2. The CSS Module is imported with the `from` syntax.
3. **Class selectors** are unique to the component. Other selectors however become global CSS rules, just like with CSS stylesheets.

## Styling our component

Create a `button.module.css` file:

```bash
touch src/components/example-5-css-modules/button.module.css
```

In the newly created `src/components/example-5-css-modules/button.module.css` file, add the following to `btn` class:


```css
/* src/components/example-5-css-modules/button.module.css */
.btn {
  background-color: #ffa500;
  border-radius: 8px;
  color: white;
  font-size: 24pt;
  padding: 15px 50px;
  width: 300px;
}
```

Now with your module setup, import your CSS module and reference its classes in your JSX as you would a normal stylesheet: 

```jsx
// src/components/example-5-css-modules/Button.jsx
import styles from './button.module.css';

const Button = ({ buttonText }) => {
  return (
    <button className={styles.btn}>
      {buttonText}
    </button>
  );
};

export default Button;
```

> 💡 Note, the class names become keys on the `styles` object