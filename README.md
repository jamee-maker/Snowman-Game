# Snowman-Game
Command-line Hangman Game.


### 1. Running the application
Click link to go to game repo: https://github.com/jamee-maker/FSW-CLI-Snowman
<ul>
  <li>Clone the repo</li>
  <li>In your terminal, cd to the cloned repo and run npm install</li>
  <li>Run node snowman.js to begin the adventure!</li>
  </ul>
  
### 2. Description of the application
<div>
This is a command-line game of Hangman. The computer picks a word at random, and the user has to guess the letters of the word until they have guessed the whole word.
  
  
  
  
  <img src="Assets/Snow intro.gif" width="700" height="400">
  
  
</div>


### 3. Remarks


<div>
  
This was the second application I ever created. This one was a whole lot harder! It required less creativity and more logical reasoning. I spent an awful amount of time rearranging my code and making sure that everything made sense because I am the type of person that likes to understand everything I'm doing down to a T. There were many challenging problems to solve and things to consider. One of them was figuring out how I was going to show the user the guesses they had already guessed.

I solved the problem by first creating an array containing an object as an element:

<img src="">


The purpose of this to to have a 'container' to hold the letters the user has already guessed. As you can see below, everytime the user guesses right or wrong, that guess will be stored in our alreadyGuessed container.


<img src="">


However I ran into a problem! If the word to be guessed has more than one of the same letter, it will add that guessed letter to our container for every time that that letter exists within it. So for example, lets say the word to be guessed is excellent. If the user guesses the letter 'e', that letter will be added to our container three times: 'e','e','e'. That's not what we want, so I had to come up with a solution:


<img src="">

In the code above, the solution was to remove duplicates. I remembered answering several questions on our Pursuit labs that involved removing duplicates from an array, so I figured I had to do the same here. I started by converting our string object into an array so that I could use an array method, which we recently learned about in class (Pursuit 7.1). Once I had an array to work with, I used the fliter method to return our converted array with the elements found only at its first index.




 
