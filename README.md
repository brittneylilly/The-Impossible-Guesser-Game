# 🎮 Game Glitch Investigator: The Impossible Guesser

## 🚨 The Situation

You asked an AI to build a simple "Number Guessing Game" using Streamlit.
It wrote the code, ran away, and now the game is unplayable. 

- You can't win.
- The hints lie to you.
- The secret number seems to have commitment issues.

## 🛠️ Setup

1. Install dependencies: `pip install -r requirements.txt`
2. Run the broken app: `python -m streamlit run app.py`

## 🕵️‍♂️ Your Mission

1. **Play the game.** Open the "Developer Debug Info" tab in the app to see the secret number. Try to win.
2. **Find the State Bug.** Why does the secret number change every time you click "Submit"? Ask ChatGPT: *"How do I keep a variable from resetting in Streamlit when I click a button?"*
3. **Fix the Logic.** The hints ("Higher/Lower") are wrong. Fix them.
4. **Refactor & Test.** - Move the logic into `logic_utils.py`.
   - Run `pytest` in your terminal.
   - Keep fixing until all tests pass!

## 📝 Document Your Experience

- [ ] Describe the game's purpose.
The game allows users 7 attempts to guess a target value in the range of 1 to 100.

- [ ] Detail which bugs you found.
1. When i enter in 1 or 0 as my guess it says go lower -- Fixed
2. When i enter in 200 is says go higher -- Fixed
4. when i click New Game, my last guess entry stays in the input box. It doesn’t clear. 
5. when “show hint” isn’t clicked it doesn’t show if i got guess correct or incorrect. 
6. when new game starts, sometimes attempts left says 7 and sometimes attempts lefts say 8
7. when I enter a guess, I have to manually clear out my entry in order to enter next entry - Fixed

- [ ] Explain what fixes you applied.
1. The first bug I fixed was to make the hint show the correctly (Go Higher or Go Lower), for guesses entered that ranged from negative infinity to 109. How i decided that this bug was actually fixed is that after updating the applicable code section in app.py, I ended the local host and re-ran the game and entered in guess values that were in between the ranges I was testing for, and checked if I received the expected output.
2. The second bug I fixed was related to the game accepting guesses that were less than 1 and greater than 100 and giving incorrect hints for some of these numbers. I added code logic to throw an error message when integers less than 1 and greater than 100 are entered.
3. The third bug I fixed was to add logic to clear the input box after i submit each entry. I added the code logic, then I ended the local host and re-ran the game. I entered in guesses and pressed the "Submit Guess" button and verified that the guess was cleared from the box. 

## 📸 Demo Walkthrough

Describe your fixed game in numbered steps so a reader can follow along without watching a video:

1. Enter a number 1 to 100
2. If a number is entered that's less than 1 or greater than 100 the game throws and error and reminds you of the range of required inputs
3. After clicking submit button, the input clears for you to type new value.
4. If you select "show hint" the game will tell you if your guess needs to be higher or lower 
5. You have 7 attempts to guess the correct number

**Screenshot** *(optional)*: <!-- Insert a screenshot of your fixed, winning game here -->

## 🧪 Test Results

```
# Paste your pytest output here, e.g.:
# pytest tests/
# ========================= X passed in 0.XXs =========================

I performed manual tests

```

## 🚀 Stretch Features

- [ ] [If you choose to complete Challenge 4, describe the Enhanced UI changes here — a screenshot is optional]
N/A
