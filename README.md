# Guess the Number

This project is a simple JavaScript game where the player tries to guess a randomly generated number. It's a fun and interactive way to practice and enhance your JavaScript skills.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Contact](#contact)

## Introduction
The "Guess the Number" game challenges players to guess a randomly selected number between 1 and 10. The game provides feedback on whether the guess is correct or not, and keeps track of the player's score.

## Features
- Simple, user-friendly interface.
- Real-time feedback on guesses.
- Score tracking.
- Alerts for winning the game.

## Getting Started
1. Clone the repository from GitHub.
2. Ensure you have a web browser to open the `index.html` file.
3. Open `index.html` in your preferred browser to play the game.

## Usage
- Enter a number between 1 and 10 in the input field.
- Click the "Check" button to see if your guess is correct.
- The result will be displayed, and your score will be updated accordingly.

## HTML Code
```html
<h1>Guess the number</h1>
<input id="guessnumber">
<button onclick="check()">Check</button>
<p id="result" style="color:green">You are wrong/right</p>
<p id="score">Score: 10</p>
<script>
    var guessnumber=document.getElementById("guessnumber")
    var result=document.getElementById("result")
    var score=document.getElementById("score")
    var randomNumber=Math.floor(Math.random()*10)+1
    var totalscore=10
    function check()
    {
        var enterednumber=guessnumber.value
        if(randomNumber==enterednumber)
        { 
            console.log("Right")
            result.textContent="Right"
            alert("YOU WON ...")
        }
        else
        {
            totalscore=totalscore-1
            console.log("Wrong")
            score.textContent="score:"+totalscore
            result.textContent="Wrong"
        }
    }
</script>
