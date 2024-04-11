# ![Styling in React - CSS Modules](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to add style to React components using CSS Modules.

## CSS Modules

**CSS Modules** offer a way to make CSS **class names** unique and specific to each component in your application. This helps avoid class name conflicts across your project.

Here’s how CSS Modules differ from regular CSS:

1. **Filename Convention**: CSS Module files are named with a `.module.css` extension. For example, instead of `button.css`, you would name it `button.module.css`.
2. **Import Syntax**: Instead of the standard CSS import, CSS Modules are imported using a specific syntax that includes from. 
   1. - For example, you would use `import styles from './button.module.css'`.
3. **Scoped Class Selectors**: Class selectors in a CSS Module are scoped to the component, meaning they won't affect other elements outside the component. However, other types of selectors (like `element` selectors) in the CSS Module behave as global rules, similar to a regular stylesheet.

By using CSS Modules, you ensure that the styles you define for one component don't unintentionally impact other parts of your application.

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
  return <button className={styles.btn}>{buttonText}</button>;
};

export default Button;
```

> 💡 Note, the class names are keys on the `styles` object we imported

Nice work! 

## Benefits and pitfalls

CSS Modules automatically ensure that all class names are local to the component, significantly reducing the risk of style conflicts. This scoping makes it easier to maintain styles across large projects, as you can be confident that changes in one component's CSS won't inadvertently impact other components.

While CSS Modules are excellent for component-level styles, managing global styles can be more complex. Developers new to CSS Modules might find it challenging to understand how to apply global styles effectively. Additionally, since CSS Modules treat non-class selectors (like `element` and `id` selectors) as global, it requires careful planning to ensure these styles don’t unintentionally affect other parts of the application.