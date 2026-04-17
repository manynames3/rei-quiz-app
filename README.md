# REI Quiz App

A lightweight quiz app built with HTML, CSS, and vanilla JavaScript.

The project presents multiple-choice questions, tracks score across a short game session, and saves high scores in the browser using `localStorage`. It is designed as a simple front-end learning project with a live, playable quiz flow and no build step required.

## Live Demo

[Open the app](https://reiquiz2.s3.amazonaws.com/index.html)

## What It Does

- Displays a landing page with links to start the quiz or view saved high scores
- Loads multiple-choice questions dynamically in the browser
- Randomizes question order and answer placement
- Awards points for correct answers
- Shows progress through the quiz with a progress bar
- Stores the most recent score and high scores locally in the browser

## Current Project Notes

The app is branded as a real-estate-investing quiz, but the current `game.js` implementation fetches general multiple-choice trivia questions from the Open Trivia Database API. There is also a local `questions.json` file in the repo, which suggests the project may have originally been intended to use a local question bank instead.

If you continue developing this project, one clear improvement would be to reconnect the quiz experience to REI-specific questions so the content matches the branding.

## Tech Stack

- HTML
- CSS
- Vanilla JavaScript
- Browser `localStorage`
- [Open Trivia Database](https://opentdb.com/) for the current question source
- Amazon S3 for hosting the live demo

## Project Structure

```text
.
├── index.html          # Landing page
├── game.html           # Quiz screen
├── game.js             # Quiz logic and scoring
├── end.html            # End-of-game screen
├── end.js              # Save score flow
├── highscores.html     # High scores page
├── highscores.js       # High scores rendering
├── app.css             # Shared styles
├── game.css            # Quiz page styles
├── highscores.css      # High scores styles
└── questions.json      # Local question bank
```

## Running Locally

Because this is a static front-end project, you can run it locally in a few simple ways:

### Option 1: Open the files directly

Open `index.html` in your browser.

### Option 2: Use a local static server

If you want a smoother local workflow, serve the project with a simple static server:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## How Scoring Works

- The game currently serves up to 3 questions per run
- Each correct answer is worth 10 points
- The final score is saved as `mostRecentScore`
- High scores are persisted in the browser, so they are device- and browser-specific

## Why This Project Exists

This repo works well as a portfolio project for practicing front-end fundamentals:

- DOM selection and updates
- Event handling
- Conditional UI feedback
- Fetching remote data from an API
- Persisting data with `localStorage`
- Building a small multi-page browser app without a framework

## Possible Next Improvements

- Replace the current trivia API questions with real estate investing questions
- Expand the local `questions.json` dataset and use it as the primary source
- Add categories or difficulty levels
- Improve mobile responsiveness and polish
- Add accessibility improvements for keyboard and screen-reader users
- Add a timer or streak system

## License

No license is currently specified in this repository.
