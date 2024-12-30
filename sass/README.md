<h1>
  <span class="headline">Styling in React</span>
  <span class="subhead">Sass</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to use Sass to style their React components.

## What is Sass?

CSS on its own can be fun, but stylesheets are getting larger, more complex, and harder to maintain. This is where a preprocessor can help. Sass has features that don't exist in CSS like nesting, mixins, inheritance, and other nifty goodies that help you write robust, maintainable CSS.

We'll let the Sass team introduce it in their own words:

_CSS on its own can be fun, but stylesheets are getting larger, more complex, and harder to maintain. This is where a preprocessor can help. Sass has features that don't exist in CSS yet like nesting*, mixins, inheritance, and other nifty goodies that help you write robust, maintainable CSS._

_Once you start tinkering with Sass, it will take your preprocessed Sass file and save it as a normal CSS file that you can use in your website._ This text is from their [getting started guide](https://sass-lang.com/guide).

> *Note that CSS now has a [nesting feature](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors#nesting) as well.

## Installing the Sass package

We'll use [the `sass` package](https://www.npmjs.com/package/sass) from npm:

```bash
npm install --save-dev sass
```

Notice the `--save-dev` flag. This indicates that this is a development dependency, but it's not a dependency for our production app. Recall the quote above: *"[...] it will take your preprocessed Sass file and save it as a normal CSS file that you can use in your website."*. The Sass package is only used during development to preprocess your Sass files into CSS files used in production.

## Creating a Sass file for our component

```bash
touch src/component/example-5-sass/button.sass
```

Once the file is created, we'll add our styles to it following the [Sass syntax documentation](https://sass-lang.com/documentation/style-rules):

```scss
// src/component/example-5-sass/button.sass

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
// src/component/example-5-sass/Button.jsx
import './button.sass';

const Button = ({ buttonText }) => {
  // Using the class name from our Sass file:
  return <button className="sassy-button">{buttonText}</button>; 
};

export default Button;
```

Here is a short list of additional tools to explore in Sass:

- Variables
- Nesting
- Mixins
- Functions
- Partials & Importing
- Inheritance
- The '`&`' Operator
- Control Directives (if else)
- Interpolation
- Placeholders

## Benefits and pitfalls

Sass introduces powerful features like variables, mixins, nesting, inheritance, and more that aren't available in standard CSS. These features allow for writing more maintainable and concise styles. Sass helps organize large style sheets efficiently and enables reusability, making managing styles in large-scale projects easier.

Sass files need to be preprocessed into standard CSS before they can be used on a website. This adds an extra step in the development process, requiring tools for compilation and potentially increasing the initial setup complexity. Newcomers to Sass may also face a learning curve in understanding its syntax and features, particularly if they're only familiar with traditional CSS.
