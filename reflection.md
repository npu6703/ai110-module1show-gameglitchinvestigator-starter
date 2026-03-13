# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the secret number kept changing" or "the hints were backwards").

- The answer was 1, but when I guessed 80 or any random number, the website kept saying "Go higher"
- When I clicked "New Game", it created new answer but when I tried to type in any number to guess and clicked "Submit Guess", the message "Game over. Start a new game to try again." is still there.
- The answer was 57, but when I guessed 54 or any random number less than 57, the website kept saying "Go lower"

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)? Copilot
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result). One correct AI suggestion was to reset the game in a cleaner way when I clicked New Game. After that change, I tested it by clicking New Game many times, and the game worked normally each time. I could type a new guess and submit without getting stuck. I also ran pytest and all tests passed.
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result). One AI suggestion first told me to clear the input box in a quick way, but that caused an error when I ran the app. So that idea looked good at first, but it was actually wrong for this app. I knew it was wrong because the app showed an error right away when I clicked New Game. Then I changed to a safer method and the error went away.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed? I checked each bug one by one in the app instead of changing everything at once. For example, I tested the Higher/Lower message by using the secret number shown in the debug section. If the hints matched the secret number, I knew that part was fixed.
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code. I ran pytest in the terminal after making changes. The tests passing showed me that the main guessing logic still worked. I also did manual tests by clicking New Game and making guesses to confirm the game did not get stuck.
- Did AI help you design or understand any tests? How? Yes, AI helped me add a test for the exact New Game bug I hit. That test was useful because it protects the fix and helps prevent the same mistake later. It also helped me understand what I should check when a state bug happens.

---

## 4. What did you learn about Streamlit and state?

- In your own words, explain why the secret number kept changing in the original app. The app was running again every time I clicked a button, so some values were getting reset by mistake. Because of that, the secret number or game status could act weird between clicks.
- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit? I would say Streamlit refreshes the script often, kind of like replaying it from top to bottom. Session state is like a memory box that keeps important values between those refreshes.
- What change did you make that finally gave the game a stable secret number? I made sure the secret number is stored in session state and only changed when starting a new game. I also reset the game in one safe place so the app state stayed consistent.

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.
