# Contributing

This is a learning tool for CPU scheduling, so readable code matters more than clever code.

I try to reply to issues within a few days.

## Development setup

It's a static site with no build step. Node is only needed for the tests and linters.

```bash
git clone https://github.com/jayhemnani9910/cpu-scheduling-algorithms.git
cd cpu-scheduling-algorithms
npm install
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Checks

CI runs all of these on every pull request:

```bash
npm test                 # algorithm tests against scheduler.js
npm run lint             # eslint
npm run format:check     # prettier
npx htmlhint index.html  # HTML lint
```

Run `npm run format` to fix formatting.

## Code style

- Match the existing style in `scheduler.js`, `script.js` and `style.css`.
- 4-space indentation in JS, HTML and CSS.
- Keep scheduling logic in `scheduler.js` with no DOM code. The UI goes in `script.js`.
- If you change algorithm logic, add or update a case in `tests/scheduler.test.js`.

## Pull requests

- Branch off `main` and open the PR against `main`.
- One issue or feature per PR. Small PRs are easier to review.
- Say what you tested in the browser.
- Update the README if user-facing behavior changes.

## Bug reports

Open an issue with the bug report template. Include the algorithm, the processes you entered (arrival times and bursts), what you expected and what you got, and your browser. A screenshot of the result helps.

## Code of Conduct

This project follows the [Contributor Covenant](CODE_OF_CONDUCT.md).
