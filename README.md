# Pre-work - *Memory Game*

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program. 

Submitted by: Jenelle Truong

Time spent: 4 hours spent in total

Link to project: https://glitch.com/edit/#!/butternut-factual-streetcar?path=index.html%3A6%3A61

## Required Functionality

The following **required** functionality is complete:

* [X] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
* [X] "Start" button toggles between "Start" and "Stop" when clicked. 
* [X] Game buttons each light up and play a sound when clicked. 
* [X] Computer plays back sequence of clues including sound and visual cue for each button
* [X] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess. 
* [X] User wins the game after guessing a complete pattern
* [X] User loses the game after an incorrect guess

The following **optional** features are implemented:

* [X] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
* [X] Buttons use a pitch (frequency) other than the ones in the tutorial
* [X] More than 4 functional game buttons
* [X] Playback speeds up on each turn
* [X] Computer picks a different pattern each time the game is played
* [X] Player only loses after 3 mistakes (instead of on the first mistake)
* [X] Game button appearance change goes beyond color (e.g. add an image)
* [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
* [ ] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

- [X] User has a limited amount of time to complete entire game

## Video Walkthrough (GIF)

If you recorded multiple GIFs for all the implemented features, you can add them here:
![](https://media.giphy.com/media/P0uRLF6OTuX7wkF8RJ/giphy.gif)
![](https://media.giphy.com/media/JMcin7lMPhBpbeI0p6/giphy.gif)
![](https://media.giphy.com/media/4QOKU8OuteAkwZbn17/giphy.gif)
![](gif4-link-here)

## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here. 
* https://developer.mozilla.org/en-US/docs/web/javascript/reference/global_objects/math/random
* https://www.w3schools.com/jsref/met_win_setinterval.asp
* https://www.w3schools.com/jsref/met_win_clearinterval.asp

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words) 

After implementing the basic features of my game, I wanted to learn more about the power of Javascript and further bring my game to life. Consequently, I challenged myself to implement a one-minute timer that counts down the time players have to complete and win the game.  

While working on the timer feature, I encountered two main issues: developing the logic for how many times the setInterval() method is called and displaying and resetting the timer at the start and end of the game. Since the timer is supposed to update every second, I first tried to call the setInterval() method within a for loop. As the for loop iterated from fifty-nine down to zero, each iteration was passed as an argument to the method that displays the number of seconds left on the webpage. However, without a way to delay each iteration by one second, the rapid execution of the for loop caused the timer to display zero as the number of seconds left. I then decided to create a global variable secsLeft instead to keep track of how many times to call the setInterval() method. By initializing secsLeft to fifty-nine and decrementing after each setInterval() call, the game would end when secsLeft reached zero. Initially, I initially elected to pass the id returned by setInterval() as an argument to the method that would call clearInterval(). However, the game continued while the timer would continue to display negative seconds after secsLeft reached zero. To give both functions access to the interval id, I decided to make a global variable to store the id and initialize the variable upon first execution of setInterval(). By utilizing global variables and referring to the Javascript basics presented in the submission tutorial, I was able to successfully create the countdown timer feature.

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words) 

From this project, I learned how HTML, CSS, and Javascript are flexible, allowing the developer to add additional functionality at any given time. As a result, the development process feels a lot more creative and opens up infinite design decisions. However, how does one approach the development process in a systematic manner when creating a website or a web application from scratch?

Meanwhile, this project also demonstrated how HTML elements can be styled by CSS rules, and how Javascript can manipulate these elements. Since vanilla Javascript already introduces so much functionality, how do Javascript libraries and frameworks differ, and what considerations are made in selecting the appropriate technology?

4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words) 

To make this game more challenging and fun for a broader audience, I would spend additional time creating modes of varying difficulty. Users would be able to select the mode of their choice by clicking on the corresponding buttons made available after clicking the start button. The most basic mode would be the game given in the tutorial. Meanwhile, in the more challenging modes, the buttons would rearrange themselves after the initial tones are played in each round. Another mode could also play a short section of a popular song with fast playback, but switch up in one of the final few rounds in an attempt to confuse the player at the last minute. I would also create modes with highly contrasting colors to be inclusive of colorblind people and audio effects at frequencies audible to those who are hard of hearing.


## Interview Recording URL Link

[My 5-minute Interview Recording](your-link-here)


## License

    Copyright Jenelle Truong

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
