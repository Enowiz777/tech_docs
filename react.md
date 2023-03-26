# React

# React Hook

## 1. Form

You can use Register Function to create a form.

*What are your goals?*
1. Less code.
2. Better validation.
3. Better errors (set, clear and display)
4. Have control over input
5. Don't deal with events.

*How do you install react-hook-form?*
- It is already installed.

*What are the rule of thumb*
1. Everything comes from useForm.
2. You use register function that connects input to the state.

*What happen if you print register function?*
{...register} will create all other things necessary such as name, onChange, and others.

- With one code <input {{...register("email")}>, it is same as
	1. Creating state
	2. Register eventlister
	3. Put eventListener value inside the input tag.

### 1.1 Watch function

# React Library

- Styled Component: 
https://styled-components.com/

# Q & A

## 1. How we handle styled

1. Global Style - import the file - all content applied
2. Modifying the styled prop directly.
3. Build CSS module - create a file with the name of the file called Module.module.css.
	- then, you can type style.className to apply the style on the Component. 

- The best way is the styled component. 

## 2. How do you fetch data efficiently

- Use React Query
https://react-query-v3.tanstack.com/

## 3. How do you create a router

- Use React-Router-Dom - lateset v6 as of 05162023

https://reactrouter.com/en/main

## 4. How do you reset css?

- use styled reset.
- you can copy and paste resetCSS.
*Where do you put the style that will be applied to the whole page?*

*How do you create a globalstyle as a component?*
import createGlobalStyle and use it.

```js
import React from 'react';
import Router from './Router';
import { createGlobalStyle } from "styled-components";

const GlobalStyle = createGlobalStyle`
@import url('https://fonts.googleapis.com/css2?family=Source+Sans+Pro:wght@300;400&display=swap');
html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, menu, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed,
figure, figcaption, footer, header, hgroup,
main, menu, nav, output, ruby, section, summary,
time, mark, audio, video {
  margin: 0;
  padding: 0;
  border: 0;
  font-size: 100%;
  font: inherit;
  vertical-align: baseline;
}
/* HTML5 display-role reset for older browsers */
article, aside, details, figcaption, figure,
footer, header, hgroup, main, menu, nav, section {
  display: block;
}
/* HTML5 hidden-attribute fix for newer browsers */
*[hidden] {
    display: none;
}
body {
  line-height: 1;
}
menu, ol, ul {
  list-style: none;
}
blockquote, q {
  quotes: none;
}
blockquote:before, blockquote:after,
q:before, q:after {
  content: '';
  content: none;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
* {
  box-sizing: border-box;
}
body {
  font-family: 'Source Sans Pro', sans-serif;
  background-color:${(props) => props.theme.bgColor};
  color:${(props) => props.theme.textColor}
}
a {
  text-decoration:none;
}
body {
	font-family: 'Inter', sans-serif;
	font-family: 'Poppins', sans-serif;
}

`;

function App() {
  return (
    <>
      <GlobalStyle />
      <Router />
    </>
  );
}

export default App;

```

*How do you install font?*

https://fonts.google.com
