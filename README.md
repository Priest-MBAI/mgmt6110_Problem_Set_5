# Internship MailBot on the Map: MGMT 6110 Problem Set 5

My individual copy of Group 7's task map, *Who Holds the Pen?*, with my own Zapier agent placed on it.

**Live page:** https://mgmt6110problemset5.vercel.app/

## What this repo is

This repo is one static web page, `index.html`, which Vercel deploys from the `main` branch. There is no build step.

The page starts from my group's Week 7 map: 13 tasks from four businesses (Modern Farmer, AI strategist, Necklace jeweller and School mail sentinel), each placed in one of four quadrants by two questions. Is there one right answer? Must people and AI work together, or can either do it alone?

For Problem Set 5 I added a fifth business, **Student internship seeker**, which is my own job. It is split into four tasks, one per quadrant. Only one of them is a built agent: **Internship MailBot**, a two-step Zap on Zapier's free plan. The other three show where AI could help next.

## Internship MailBot at a glance

| | |
|---|---|
| Job | Tell me when an email shows an internship opening, or an update on an internship I applied for. |
| Trigger | Gmail, new email matching a search: any form of the word *internship*. It skips any email whose subject contains "Internship Alert", the subject it gives its own alerts, so a forwarded alert cannot set it off again. Side effect: a portal mailer with that same subject would be skipped too. |
| Action | Email by Zapier sends me one alert, with the matched email's subject, sender, date and a link to open it. |
| It must never | Email anyone but me. The recipient is fixed, and there is no reply or forward step. |
| Person in the loop | Me: I read every alert and decide whether it is an opening, an update or noise. |
| Quadrant | Agents run it, a person judges. |

## What is on the page, top to bottom

1. **The map.** Filters for each business, and the four quadrants with each task as a coloured card. My four tasks are already placed when the page opens.
2. **My agent card**, in the PS5 format.
3. **Runs**, each checked against Zap history, with what I expected written before each test.
4. **Q1, parts (a) to (d)**: my quadrant, the two questions with evidence from my runs, the person in the loop, and my view of my group's placements.
5. **Collaboration log**: what I delegated to AI, what I checked, one AI error I caught, and time and cost.
6. **Reflection and version history** of the Zap.

## Play the walkthrough

Press **Play walkthrough**. It steps through the two questions, the four quadrants and then each business's tasks, which takes about two minutes. A bar at the bottom shows the current step, the part to read is highlighted, and **Stop** ends it at any time.

Problem Set 5 does not ask for a video. If you want a recording anyway, start a screen recording (Cmd+Shift+5 on a Mac) and then press Play walkthrough.

## Versions of the Zap

| Version | When (Singapore time) | What changed |
|---|---|---|
| v1 and v2 | 17 Oct 2026, live by 6:37 PM | First build: a search for my date phrase, with an alert by Email by Zapier. |
| v3, "Role filter fix" | 18 Oct 2026, 2:17 AM | Added my role words after a marketing internship fired. |
| v4, "v4 broad internship catch" | 18 Oct 2026, about 12:14 PM | Any form of the word, openings and updates alike; skips subjects containing "Internship Alert"; puts the matched subject in the alert. Tested at 1:10 PM: an update and an "Intern" opening fired, a forwarded alert was skipped. |

## Evidence and privacy

- The Zap history JSON (`PS5_Asman_Alan_zap_history.json`) went to the instructor on eLearn. It is deliberately not in this repo, as Problem Set 5 asks.
- The page shows no email addresses and no Zapier "stop these emails" links.
- The **Run Zap** buttons on the map are demos. `ZAPIER_HOOK_URL` in `index.html` is empty, so they only log the task's details in the browser console.

## Updating the page

Edit or upload `index.html` on GitHub and commit to `main`. Vercel redeploys within about a minute. Then check the live page in a private window, which confirms it opens without a sign-in.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole page: map, walkthrough and my Problem Set 5 sections. |
| `PLAN.md`, `sentinel/` | Carried over from the group project: the plan and setup guides for the School mail sentinel. They are not part of Internship MailBot. |
| `.gitignore` | Keeps local files out of the repo. |

## Credits

The quadrant framework and agent loop come from Roh, S. (2026), MGMT 6110 Week 7, *The Map of Human-AI Collaboration* and *Building AI Agents I*, SMU. The map, the first 13 tasks and their placements are my group's work. The Student internship seeker tasks, Internship MailBot and the Problem Set 5 sections are mine.
