# Password Generator App

This is a solution to the [Password generator app challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/password-generator-app-Mr8CLycqjh). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

This project was built with React.js, Redux, JavaScript, Sass and tested with Jest, and it's hosted [here](https://password-generator.spomberg.com).

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
- [Built with](#built-with)
- [What I learned](#what-i-learned)
  - [Work with detailed wireframes](#work-with-detailed-wireframes)
  - [Test Driven development practice](#test-driven-development-practice)
  - [React Redux](#react-redux)
  - [Recursion](#recursion)
- [Author](#author)

## Overview

Password Generator App is a responsive single-page site built with React. Users are able to:

- Generate a password based on the selected inclusion options
- Copy the generated password to the computer's clipboard
- See a strength rating for their generated password
- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page

### The challenge

The challenge was to create the app based solely on the user stories above and the design files provided. I was free to use any framework and language I wished and no code was given to start with.

The image below is the provided preview of what the app was supposed to look like:

![preview](https://github.com/spomberg/password-generator-app/blob/main/docs/preview.jpg?raw=true)

### Screenshot

And these are gifs showing the final product in action:

Desktop

![desktop-demo](https://github.com/spomberg/password-generator-app/blob/main/docs/password-generator.gif?raw=true)

Mobile

![mobile-demo](https://github.com/spomberg/password-generator-app/blob/main/docs/password-generator-mobile.gif?raw=true)

## Built with

- React
- Sass
- JavaScript
- MaterialUI

### Dependencies

- React-Redux
- MaterialUI
- React Copy to Clipboard
- React SVG
- Jest

## What I learned

### Work with detailed wireframes

This challenge allowed me to flex my frontend skills, I was able to bring industry-level designs to life, I'm most proud of how close the final product is to the wireframes provided.

### Test-Driven Development practice

The helper functions are the heart of this app, they generate the randomized password string and verify that it's valid. I used Jest and followed a test-driven workflow to ensure the results matched the expected outcome.

### React Redux

Although I had solid experience with React beforehand, one thing that I had relied on in the past on frontend projects was prop drilling, which makes the code confusing and hard to maintain. Right at the beginning I decided I was going to learn how to use React Redux to control states and make my code cleaner. I'm proud to say I understand the concept now and am will be using it on React projects moving forward.

### Recursion
A concept that I had always struggled to grasp is recursion and I was really happy to find a practical use for it inside the main helper function and I feel that I finally understand it now. 

The generatePassword function creates a random password string based on the settings provided by the user, however, the string must contain at least one character from each category selected.

I used another helper function to verify if the password is valid and if it's not I call generatePassword to generate another random string to be verified again and so on until the result is valid.

```js
function generatePassword(length, hasUpperCase, hasLowerCase, hasNumbers, hasSymbols) {

  //(...)

  if (!isPasswordValid(result, hasUpperCase, hasLowerCase, hasNumbers, hasSymbols)) {

    return generatePassword(length, hasUpperCase, hasLowerCase, hasNumbers, hasSymbols);
  
  }

  else return result;

}
```

## Author

AWS Certified Web Developer with a knack for finding innovative solutions for solving complex problems in a timely manner. 

Throughout my career, I have honed my people skills in other industries where I successfully led projects in different areas. I also trained hundreds of people, as passing down knowledge (while continuously learning) is a passion of mine. 
  
Aside from my passion for coding, my abilities also extend to communication and collaboration with proficiency in interpersonal skills. My strongest suit is that I can bring these two skill sets together in a unique way. 
  
My goal is to now use my skills to make meaningful connections, exchange knowledge and help others while working as a Web Developer.

- Portfolio - [spomberg.com](https://spomberg.com)
- LinkedIn - [/marcos-spomberg](https://www.linkedin.com/in/marcos-spomberg/)

## Other projects

- My Movie List - [Site](https://mymovielist.ca) / [Repo](https://github.com/spomberg/my-movie-list)
- Memory Game - [Site](https://memory.spomberg.com) / [Repo](https://github.com/spomberg/memory)
