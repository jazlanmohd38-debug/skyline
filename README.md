# ✦ Skyline: AI-Powered Personalized Learning & Career Guidance

Skyline turns a learner's skills into a **constellation**. Specialized AI agents find the missing stars for a target career and draw the shortest learning path to it.

## Features
- Sign up / log in, profile (education, experience, skills, certifications, projects, cover photo)
- 8 career goals (Full Stack, Frontend, Backend, Data Scientist, AI/ML, UI/UX, Cybersecurity, Cloud)
- AI skill-gap analysis with a skill-constellation visual and match %
- Personalized roadmap: levels, prerequisites, durations, exercises, mini and final projects, resource links
- Progress dashboard: roadmap %, quiz scores, skill improvement, weekly activity
- AI Mentor chatbot that uses the learner's profile, gaps, progress and scores
- Light/dark mode, live typography studio, animated backgrounds
- **One-click demo** on the landing page (Python, SQL, basic HTML → Full Stack Developer)

## Multi-agent architecture
| Agent | Job |
|---|---|
| Career Analysis Agent | Lists the skills and levels a role requires |
| Skill Analysis Agent | Compares the learner against the role; strengths and weaknesses |
| Learning Recommendation Agent | Builds the ordered roadmap with exercises and projects |
| Progress Evaluation Agent | Generates quizzes, scores them, tracks progress |
| AI Mentor Agent | Personalized guidance using all of the above |
| Coordinator | Runs the agents in order and re-plans on events |

**Adaptive behavior:** changing the career goal rebuilds the roadmap; a quiz score under 60% inserts a remedial block; 80% or more unlocks the next level; completing a step updates skill levels and match %.

## Run it
It is a single static file. Open `index.html` in a browser (or use the GitHub Pages link).

1. Create an API key at https://platform.openai.com/api-keys
2. In the app: **Settings → OpenAI API key → Save key**
3. Click **▶ Try the demo scenario** on the landing page

The key stays in your browser's localStorage and is never committed to the repo.

## Deploy on GitHub Pages
Repo **Settings → Pages → Deploy from a branch → `main` / root**. Your site appears at `https://<username>.github.io/<repo>/`.

## Notes
- Accounts and progress are stored locally in the browser (demo-grade authentication).
- Resource links point to YouTube, Coursera and documentation searches for each skill.

## Tech
Vanilla HTML/CSS/JS, canvas background, SVG charts, OpenAI Chat Completions API (`gpt-4o-mini`).
