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
2. **Find the State Bug.** Why does the secret number change every time you click "Submit"? Ask ChatGPT: _"How do I keep a variable from resetting in Streamlit when I click a button?"_
3. **Fix the Logic.** The hints ("Higher/Lower") are wrong. Fix them.
4. **Refactor & Test.** - Move the logic into `logic_utils.py`.
   - Run `pytest` in your terminal.
   - Keep fixing until all tests pass!

## 📝 Document Your Experience

- [x] Describe the game's purpose. This game is a simple number guessing game where the player tries to guess a secret number in a limited number of tries. The game gives a hint after each guess to help the player get closer.
- [x] Detail which bugs you found. At first, the hints were wrong, so the game told me to go higher when my guess was already too high (and the opposite too). Also, after clicking New Game, the app sometimes still acted like the old game was over and did not let me keep playing normally.
- [x] Explain what fixes you applied. I fixed the guess-checking logic so higher and lower hints match the real answer. I also fixed how New Game resets values so the game starts fresh and works right away. After that, I ran pytest and all tests passed.

## 📸 Demo

- [x]![alt text](image.png) [Insert a screenshot of your fixed, winning game here]

## 🚀 Stretch Features

- [ ] [If you choose to complete Challenge 4, insert a screenshot of your Enhanced Game UI here]
