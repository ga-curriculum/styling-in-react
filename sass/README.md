# ![Styling in React - Sass](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to use Sass to style their React components.

## Using Sass

CSS on its own can be fun, but stylesheets are getting larger, more complex, and harder to maintain. This is where a preprocessor can help. Sass has features that don't exist in CSS yet like nesting, mixins, inheritance, and other nifty goodies that help you write robust, maintainable CSS.

_Once you start tinkering with Sass, it will take your preprocessed Sass file and save it as a normal CSS file that you can use in your website..._ [source](https://sass-lang.com/guide)

![sass](https://sass-lang.com/assets/img/styleguide/color-1c4aab2b.png)

## Installing the Sass package

We'll be using [this package](https://www.npmjs.com/package/sass) to install Sass.

```bash
npm install --save-dev sass
```

## Creating a Sass file for our component

```bash
touch src/component/example-6-sass/button.sass
```

Once the file is created we'll add our styles to it using the [sass syntax documentation](https://sass-lang.com/documentation/style-rules):

```scss
// src/component/example-6-sass/button.sass
$sass-pink: #ce649a
$bright: hotpink

.sassy-button
  background-color: $sass-pink
  border-radius: 8px
  color: white
  font-size: 24pt
  padding: 15px 50px
  width: 300px

  &:hover
    background-color: $bright
```

## Importing and using Sass

```jsx
// src/component/example-6-sass/Button.jsx
import './button.sass';

const Button = ({ buttonText }) => {
  return <button className="sassy-button">{buttonText}</button>; // using the class name from our Sass file
};

export default Button;
```

Here is a short list of things to explore in Sass:

- Variables
- Nesting
- Mixins
- Functions
- Partials & Importing
- Inheritance
- The '&' Operator
- Control Directives (if else)
- Interpolation
- Placeholders

## Benefits and pitfalls

Sass introduces powerful features like variables, mixins, nesting, inheritance, and more, that aren’t available in standard CSS. These features allow for writing more maintainable and concise styles. Sass helps in organizing large stylesheets efficiently and enables reusability, making it easier to manage styles in large-scale projects.

Sass files need to be preprocessed into standard CSS before they can be used in a website. This adds an extra step in the development process, requiring tools for compilation and potentially increasing the initial setup complexity. Newcomers to Sass may also face a learning curve in understanding its syntax and features, particularly if they're only familiar with traditional CSS.

**Congrats You now know 6 different ways to style React components!**