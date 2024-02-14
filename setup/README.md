# ![Styling in React - Setup](./assets/hero.png)

## Setup

Open your Terminal application and navigate to your **`~/code/ga/lectures`** directory:

```bash
cd ~/code/ga/lectures
```

Create a new Vite project for your React app:

```bash
npm create vite@latest
```

You'll be prompted to choose a project name. Let's name it `styling-in-react`. 

- Select a framework. Use the arrow keys to choose the `React` option and hit `Enter`.

- Select a variant. Again, use the arrow keys to choose `JavaScript` and hit `Enter`.

Navigate to your new project directory and install the necessary dependencies:

```bash
cd styling-in-react
npm i
```

Open the project's folder in your code editor:

```bash
code .
```

### Configuring ESLint

Before we begin, we need to adjust the ESLint configuration. Add the following rules to the `.eslintrc.cjs` file:

```js
rules: {
  'react-refresh/only-export-components': [
    'warn',
    { allowConstantExport: true },
  ],
  'react/prop-types': 'off', // add this line
  'react/no-unescaped-entities': 'off' // add this line
},
```

The first addition prevents warnings if you're not declaring types for your props (which we're not), and the second prevents warnings if you're using contractions within JSX.

### Clear `App.jsx`

Open the `App.jsx` file in the `src` directory and replace the contents of it with the following:

```jsx
// src/App.jsx

const App = () => {

  return (
    <h1>Hello world!</h1>
  );
}

export default App
```

### GitHub setup

To add this project to GitHub, initialize a Git repository:

```bash
git init
```

Make a new repository on [GitHub](https://github.com/) named [tktk-module-name]. 

Link your local project to your remote GitHub repo:

```bash
git remote add origin https://github.com/<github-username>/[tktk-module-name].git
git push origin main
```

> 🚨 Do not copy the above command. It will not work. Your GitHub username will replace `<github-username>` (including the `<` and `>`) in the URL above.


Open the contents of the directory in VSCode:

```bash
code .
```

### Directory setup

Add a directory called `components` inside `src`

```bash
mkdir src/components
```

Add the following directories inside of `components`:

  - example-1-normal-css
  - example-2-inline-css
  - example-3-css-in-js
  - example-4-styled-components
  - example-5-css-modules
  - example-6-sass

```bash
mkdir src/components/example-1-normal-css src/components/example-2-inline-css src/components/example-3-css-in-js src/components/example-4-styled-components src/components/example-5-css-modules src/components/example-6-sass
```


### Creating the Button Components

We will be re-creating the same component file inside each of these example component folders. This will act as our "starter code" for each of today's examples. 

_Note:_ Typically purpose of components is reusability, however, because they all have different methods of incorporating thier styles and css - we will be recreating the same component for each example.


Create a Button.jsx file in each of the example folders ( 6 total ).

```bash
touch src/components/example-1-normal-css/Button.jsx
touch src/components/example-2-inline-css/Button.jsx
touch src/components/example-3-css-in-js/Button.jsx
touch src/components/example-4-styled-components/Button.jsx
touch src/components/example-5-css-modules/Button.jsx
touch src/components/example-6-sass/Button.jsx
```

Include the following code in your Button files:

```jsx
const Button = ({ buttonText }) => {
  return (
    <button>{ buttonText }</button>
  )
}

export default Button
```

Now we'll modify `App.js` and get it ready for our examples: 

`App.js`:
```javascript
import './App.css';
// import button components here

const App = () => {
  return (
    <div className='App'>
      {/* Add example components here */}
    </div>
  );
}

export default App;
```

Lets also add some of our own default styles to `App.css`:

`App.css`:
```css
/* import fonts */
 

* {
  /* add custom fonts here */
}

.App {
  display: flex;
  flex-direction: column;
  gap: 30px;
  margin: 0 auto;
  width: 300px;
}
```

Lets go get a cool Roboto font from [google fonts](https://fonts.google.com/specimen/Roboto+Flex).

Import your fonts in `App.css` and add your font family styles to '*'.

`App.css`:
```css
/* import fonts */
@import url('https://fonts.googleapis.com/css2?family=Roboto+Flex:opsz,wght@8..144,100..1000&display=swap');


* {
  /* add custom fonts here */
  font-family: 'Roboto Flex', sans-serif;
}

.App {
  display: flex;
  flex-direction: column;
  gap: 30px;
  margin: 0 auto;
  width: 300px;
}
```

With each example we'll import a new button component to our `App.js` like this:

 ```jsx
 <ButtonOne text="Example 1" />
 ```

### Lets get styling...

For the following examples we'll be using the same set of base styles ( with minor variations ) in our button components. 

You'll want to refer back to these: 

```css
.default-button {
  background-color: white;
  border-radius: 8px;
  color: blue;
  font-size: 24pt;
  padding: 15px 50px;
  width: 300px;
}
```