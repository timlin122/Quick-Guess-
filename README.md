# The Game
`Quick, Guess!` is a word/phrase guessing game (commonly known as *hangman*). This game currently supports up to two players and is under development.
## Our Goal
With this game, we hope to be able to provide a resource that may help kids learn **new vocabulary** and get a **deeper understanding** of words in a **fun** and **engaging** way.
## Quick Overview
As of right now, two players are able to play competitively in this word guessing game. Each player takes turns  guessing the words while making sure not to lose any lives. Last one standing wins the game!
### How to Win
Since this is a competitive game which people tend to enjoy, it's necessary to know how to crush your opponent! Each player has _3 lives_ (will change in upcoming gamemodes) and may lose a life if the word is not guessed before the timer runs out or if they guess too many incorrect letters. Be the one with lives at the end, to claim your victory!
### Abilities (Under Development)
To add more *spice* to the game, there are more comlpications and things you can do. One such thing would be perks, which may be gained randomly after surviving a round without losing any lives. These perks could either be used for personal benefit or sabotaging your opponent by doing the following:
- Gaining more time
- Gaining more incorrect guess chances
- Decreasing your opponent's time
- Lowering incorrect guess chances for your opponent
More abilities will be on their way!
### Pseudocode
**Setup:**
- Create canvas to window size
- Display the player boxes, bomb, timer, arrow, lives, pause button, instruction button, option for the modes and the boxes for incorrect guesses

**UI Loop:**
- __If__ n player mode is selected, 
     Create a back button is home screen
     Create a button for grade 1 mode
     Create a button for medium mode
     Create a button for hard mode
     
- __If__ grade 1 mode is clicked,
	Create a button to go back to other modes
        Pick a word out of the existing grade 1 word bank (much easier words)
  Lives for each player is set to 5
  Timer is set to 90 
  Arrow is pointed to player 1
 - __If__ player 1 guesses a letter correctly, 
    The letter appears in the index of the prompt (replacing the underscore)
 -  __If__ player 1 guesses incorrectly, 
    The letter gets added to the incorrect guesses array
 - __If__ player 1 guesses 3 letters wrong or the timer hits 60,
    Hint associated with word is displayed
    Image associated with the word is displayed
 - __If__ player 1 guesses a letter again, 
    Prints “You’ve already guessed this!”
 - __If__ player 1 guesses the word right, 
    The arrow switches to the other player, 
    Timer resets, 
    New word is picked,
    Random spin for a chance at perks (more incorrect guess boxes, more time, etc.)
 - __If__ a player gets more than allowed incorrect guesses (9 if no perks have been used) or timer runs out before word is guessed, 
    Bomb explodes,
    The player loses a life,
    Timer resets, 
    Arrow switches to next player
 - __If__ timer is reset any n times, where n can be divided by 2, 
    The bomb starting timer decreases by 5
 - __If__ the starting timer hits 10, 
    It will stop decreasing per round and stay at 10
 - __If__ a player has lost all their lives
    The player is eliminated and n-1 players continue the game
 - __If__ n-1 players are eliminated
    The remaining player wins the game and gets a compliment 👍
    The game is over and the player with at least 1 life wins (prints “Player n has won!”)
    
- __If__ medium mode is clicked,
  Create a button to go back to other modes
  Pick a word out of the existing medium word bank
  Lives for each player is set to 3
  Timer is set to 60 
  Arrow is pointed to player 1
- __If__ player 1 guesses a letter correctly, 
    The letter appears in the index of the prompt (replacing the underscore)
- __If__ player 1 guesses incorrectly, 
    The letter gets added to the incorrect guesses array
- __If__ player 1 guesses a letter again, 
    Prints “You’ve already guessed this!”
- __If__ player 1 guesses the word right, 
    The arrow switches to the other player, 
    Timer resets, 
    New word is picked,
    Random spin for a chance at perks (more incorrect guess boxes, more time, etc.)
- __If__ a player gets more than allowed incorrect guesses (7 if no perks have been used) or timer runs out before word is guessed, 
    Bomb explodes,
    The player loses a life,
    Timer resets, 
    Arrow switches to next player
- __If__ timer is reset any n times, where n can be divided by 2, 
    The bomb starting timer decreases by 5
- __If__ the starting timer hits 7, 
    It will stop decreasing per round and stay at 7
- __If__ a player has lost all their lives
    The player is eliminated and n-1 players continue the game
- __If__ n-1 players are eliminated
    The remaining player wins the game and gets a half-hearted compliment 👍
    The game is over and the player with at least 1 life wins (prints “Player n has won!”)

- __If__ hard mode is clicked,
	Create a button to go back to other modes
  Pick a word out of the existing medium word bank
  Lives for each player is set to 3
  Timer is set to 30
  Arrow is pointed to player 1
- __If__ player 1 guesses a letter correctly, 
    The letter appears in the index of the prompt (replacing the underscore)
- __If__ player 1 guesses incorrectly, 
    The letter gets added to the incorrect guesses array
- __If__ player 1 guesses a letter again, 
    Prints “You’ve already guessed this!”
- __If__ player 1 guesses the word right, 
    The arrow switches to the other player, 
    Timer resets, 
    New word is picked,
    Random spin for a chance at perks (more incorrect guess boxes, more time, etc.)
- __If__ a player gets more than allowed incorrect guesses (7 if no perks have been used) or timer runs out before word is guessed, 
    Bomb explodes,
    The player loses a life,
    Timer resets, 
    Arrow switches to next player
- __If__ timer is reset any n times, where n can be divided by 2, 
    The bomb starting timer decreases by 5
- __If__ the starting timer hits 5, 
    It will stop decreasing per round and stay at 5
- __If__ a player has lost all their lives,
    The player is eliminated and n-1 players continue the game
- __If__ n-1 players are eliminated,
    The remaining player wins the game and gets insulted 👍
    The game is over and the player with at least 1 life wins (prints “Player n has won!”)



## Features
- [x] Randomly chosen word(s)
- [x] Ability to guess words
- [x] A temporary functional timer
- [ ] A permanent functional timer
- [ ] Perks
- [ ] Gamemodes
- [ ] Lives/Scoring system
- [ ] More abilities
- [ ] Sound
- [ ] Visual Effects
