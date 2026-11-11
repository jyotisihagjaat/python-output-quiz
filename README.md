# 🐍 Predict the Output

A timed Python quiz where you read a short piece of code and pick what it prints. 15 tricky questions, 3 lives, and an explanation after every answer.

### 🎮 [Play it now](https://jyotisihagjaat.github.io/python-output-quiz)

## Why I built it

Many Python bugs come from small surprises in the language, not from hard algorithms. This quiz turns those surprises into a game, so you can practise spotting them before they show up in an interview or in production.

## How to play

- You see a Python snippet and four possible outputs.
- You have 20 seconds to choose.
- Correct answers score points. Faster answers and longer streaks score more.
- You have 3 lives. Three wrong answers (or timeouts) end the game.
- After every question, a short explanation tells you why the answer is what it is.
- At the end you get a rank, from **Intern** to **Staff Engineer**, and a button to copy your result.

## Topics covered

- Floating point precision
- Truthiness of values
- Floor division and rounding
- Mutable vs immutable objects
- Mutable default arguments
- Variable scope (`UnboundLocalError`)
- List multiplication and shared references
- Late binding in lambdas
- String comparison
- Sets and hashing

## Built with

- HTML, CSS and vanilla JavaScript
- No frameworks and no libraries
- `localStorage` to save your best score
- GitHub Pages for hosting

## Run it locally

```bash
git clone https://github.com/jyotisihagjaat/python-output-quiz.git
cd python-output-quiz
```

Open `index.html` in any browser. There is nothing to install.

## Add your own questions

Questions live in one array called `Q` inside `index.html`. Each question looks like this:

```js
{
  c: "print(len({1, 1.0, True}))",   // the code shown to the player
  o: ["3", "2", "1", "Error"],       // the four options
  a: 2,                              // index of the correct option
  e: "1 == 1.0 == True, so the set keeps only one."  // explanation
}
```

Add an object, save the file, and refresh the page.

## Roadmap

- [ ] Difficulty levels (easy, medium, hard)
- [ ] Topics: decorators, generators, closures
- [ ] Daily challenge question
- [ ] Online leaderboard

## Contributing

Found a better trick question or a mistake in an explanation? Open an issue or send a pull request. Good questions are very welcome.

## License

MIT
