# ![Styling in React - tktk Microlesson Name](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to tktk

#### Example 6 : Sass

<br>

*CSS on its own can be fun, but stylesheets are getting larger, more complex, and harder to maintain. This is where a preprocessor can help. Sass has features that don't exist in CSS yet like nesting, mixins, inheritance, and other nifty goodies that help you write robust, maintainable CSS.*

*Once you start tinkering with Sass, it will take your preprocessed Sass file and save it as a normal CSS file that you can use in your website...* [source](https://sass-lang.com/guide)

![sass](https://sass-lang.com/assets/img/styleguide/color-1c4aab2b.png)

We'll be using [this package](https://www.npmjs.com/package/sass) to install Sass.


This package is a distribution of Dart Sass, compiled to pure JavaScript with no native code or external dependencies. It provides a command-line sass executable and a Node.js API.

You can install Sass globally using `npm install -g sass` which will provide access to the sass executable. You can also add it to your project using `npm install --save-dev sass`

We'll be using the second option.

Create a new file in your component example folder called `button.sass`

Add your default button styles using the [sass syntax documentation](https://sass-lang.com/documentation/style-rules).

Import your sass file in your button component just like a normal css file. 

```jsx

import "./button.sass"

export default function Button({ text }) {
  return <button className="sassy-button">{ text }</button>;
}

```

Some fun things to explore in sass -

  -Variables
  -Nesting
  -Mixins
  -Functions
  -Partials & Importing
  -Inheritance
  -The '&' Operator
  -Control Directives (if else)
  -Interpolation
  -Placeholders

✨  Let's give it a fancy background-color: #ce649a

✨  Bonus: refector to accept props and add a prop style

<br>
<br>

#### Review Questions

**❓ What is sass?**

**❓ Are there extra tools required when using a CSS preprocessor like Sass?**

**❓ Why is sass so popular?**


<br>
<br>

**You now know 6 different ways to style react components!**

#### Which was your favorite?
