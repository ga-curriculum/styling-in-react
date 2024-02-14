# ![Styling in React - Setup](./assets/hero.png)

## Setup

Open your Terminal application and navigate to your **`~/code/ga/lectures`** directory:

```bash
cd ~/code/ga/lectures
```

Make a new directory called **`[styling-in-react]`**, then enter this directory:

```bash
mkdir [styling-in-react]
cd [styling-in-react]
```

<!-- Other setup instructions here -->


Open the contents of the directory in VSCode:

```bash
code .
```


#### Set Up - 5 min 

Create a new react app for todays codealong:

`npx create-react-app@latest react-css`

1. Add a directory called `components` inside `src`

2. Add the following directories inside of `components`:

  - example-1-normal-css
  - example-2-inline-css
  - example-3-css-in-js
  - example-4-styled-components
  - example-5-css-modules
  - example-6-sass


<br><br>

#### Creating the Button Components

We will be re-creating the same component file inside each of these example component folders. This will act as our "starter code" for each of today's examples. 

_Note:_ Typically purpose of components is reusability, however, because they all have different methods of incorporating thier styles and css - we will be recreating the same component for each example.

#### More Set Up - 2 min

Create a Button.jsx file in each of the example folders ( 6 total ).

Include the following code in your Button files:

```javascript
export default function Button({ buttonText }) {
  return (
    <button>{ buttonText }</button>
  );
}
```

Now lets clean up App.js and get it ready for our examples: 

`App.js`

```javascript
import "./App.css";
// import button components here

function App() {
  return (
    <div className="App">
      {/* Add example components here */}
    </div>
  );
}

export default App;
```

Lets also wipe out App.css and add some of our own default styles:

`App.css`



```css
/* import fonts  */ 


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

<br>
<br> 

With each example we'll import a new button component to our `App.js` like this:

 ```javascript
 <ButtonOne text="Example 1" />
 ``` 

<br>
<br> 


#### Lets get styling...

<br>
<br>

For the following examples we'll be using the same set of base styles ( with minor variations ) in our button components. 

You'll want to refer back to these: 

<br>

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

<br>
<br>