# ![Styling in React - Concepts](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will have a broad understanding of the available options for styling in a React application.

## Overview of styling in React

Like many things in React, styling is done a little differently than what we've become accustomed to.

There are several popular methods for styling react components, what you choose to use in your applications is up to you. There is no true "industry standard" and exposure to multiple styles and examples is ideal. In a real job setting, you will just adopt whatever libraries or conventions are used in the existing codebase.

## Some options for styling React components

In this module, we will look at a few of the more popular ways to style React components:

1. **Imported CSS Stylesheets**: This is the approach that `Vite` uses with its `<App>` component by default. Each component has a designated CSS file.

2. **Inline Styling**: This approach uses the `style` prop.

3. **CSS in JS**: Requires a package: `npm install react-jss`.

    [React-JSS](https://cssinjs.org/react-jss/?v=v10.9.0) integrates JSS with React using the new Hooks API.

4. **Styled Components**: Requires a package: `npm install styled-components`.

    [Styled-Components](https://www.npmjs.com/package/styled-components):  _"Utilizes tagged template literals (a recent addition to JavaScript) and the power of CSS, styled-components allows you to write actual CSS code to style your components... Styled-components is compatible with both React (for web) and React Native – meaning it's the perfect choice even for truly universal apps!"_

5. **CSS Modules**: Similar to importing regular stylesheets, but different in a significant way - scoping. CSS files are included the same way but with the following file extension format `filename.module.css`. CSS written in this module will be scoped locally to the component that is importing it. This can help avoid class name collisions in large applications.

6. **SASS**: Requires a package: `npm install sass`.

    [Sass](https://sass-lang.com/): Sass is the most mature, stable, and powerful professional grade CSS extension language in the world.
