# The Nightmare Before Deployment
A 15-question, host-controlled, real-time Halloween trivia game for 12 remote developers.

## Deploy to Render
1. Push this folder to a private GitHub repository (or deploy via your preferred Git workflow).
2. Render → New → Web Service → connect repository.
3. Runtime: Node; Build command: `npm install`; Start command: `npm start`.
4. Add environment variable `HOST_PASSWORD` with a long, unique password.
5. Choose a plan and deploy. Free services may spin down when idle; open the app before the meeting.
6. Visit `https://YOUR-SERVICE.onrender.com/host.html`, sign in, and share that screen in Teams.
7. Staff visit `https://YOUR-SERVICE.onrender.com/`, enter nicknames, and play.

## Run locally
Node.js 20+ required. Run `npm install`, set `HOST_PASSWORD`, and run `npm start`. Visit `http://localhost:3000/host.html`.

## Gameplay
- 15 questions, 3 rounds of 5.
- Each question lasts 25 seconds, or host may reveal early.
- 100 base points plus speed bonus (up to 125); question 10 is worth double points.
- The host manually advances between questions and rounds.
- Reset Scores keeps players; Clear Players starts fresh.
- Players reconnect using a saved local browser ID. Scores live in server memory and reset if Render restarts.

## Notes
Do not include confidential work data in nicknames or questions. Host password is checked server-side; keep it out of Git. This is designed for one small, friendly game, not high-stakes or adversarial use. Test with two browser windows before the meeting.
