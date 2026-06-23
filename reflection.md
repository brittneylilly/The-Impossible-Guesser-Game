# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?

The game screen had "Make a guess" and then the subtext to that said "Guess a number between 1 and 100. Attempts left: 7

- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").

1. When i enter in 1 or 0 as my guess it says go lower -- Fixed
2. When i enter in 200 is says go higher -- Fixed
4. when i click New Game, my last guess entry stays in the input box. It doesn’t clear. 
5. when “show hint” isn’t clicked it doesn’t show if i got guess correct or incorrect. 
6. when new game starts, sometimes attempts left says 7 and sometimes attempts lefts say 8
7. when I enter a guess, I have to manually clear out my entry in order to enter next entry - Fixed


**Bug Reproduction Log**

Document at least 3 bugs you found. Add rows as needed.

| Input | Expected Behavior | Actual Behavior | Console Output / Error |
|-------|-------------------|-----------------|------------------------|
| 1     | "Go Higher"         "Go Lower"          None
| 0     | "Go Higher"         "Go Lower"          None  
| 200   | "Go Lower"          "Go Higher"         None

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
Gemini 

- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
Gemini suggested that I needed to add a new method to help with handling clearing the input box after each submission.
It was correct that I needed this method. I verified the result by testing a range of input numbers.

- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).
Gemini was incorrect in where i needed to place this method inside my code. 

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?

1. The first bug I fixed was to make the hint show the correctly (Go Higher or Go Lower), for guesses entered that ranged from negative infinity to 109. How i decided that this bug was actually fixed is that after updating the applicable code section in app.py, I ended the local host and re-ran the game and entered in guess values that were in between the ranges I was testing for, and checked if I received the expected output.
2. The second bug I fixed was related to the game accepting guesses that were less than 1 and greater than 100 and giving incorrect hints for some of these numbers. I added code logic to throw an error message when integers less than 1 and greater than 100 are entered.
3. The third bug I fixed was to add logic to clear the input box after i submit each entry. I added the code logic, then I ended the local host and re-ran the game. I entered in guesses and pressed the "Submit Guess" button and verified that the guess was cleared from the box. 

- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.

I ran manual tests as outlined in previous response

- Did AI help you design or understand any tests? How?

N/A

---s

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
With python you have to import import streamlit as st and you must use st. to implement most programming operations within the Streamlit app.

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.

Documenting the bugs I see in a table, and taking an incremental approach to fixing each bug one by one and testing
as I go.

- What is one thing you would do differently next time you work with AI on a coding task?
N/A

- In one or two sentences, describe how this project changed the way you think about AI generated code.
This project has not changed the way I think about AI generated code.
