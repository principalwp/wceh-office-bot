# wceh-office-bot

A pipeline is a list of steps your AI follows, written in a text file. This repo has the finished `wceh-office-bot` (set up for everyday office tasks) and the `wceh-office-bot-starter`, an empty template that you fill in during the workshop.

The bot has eight steps: confirm intent, research, write the plan, plan approval, implement, review and fix, finished, learn. Five of them hand work to a worker (the researcher, the planner, the implementer, the reviewer and Learn).

## Exercise 1: Get your bot

Pick your tool. Whatever the tool, call the bot by starting your message with its name, for example `wceh-office-bot: <task>`.

| Your tool | What to do |
|---|---|
| Claude Code | `git clone https://github.com/principalwp/wceh-office-bot.git` then `cd wceh-office-bot && claude`. Approve the folder-trust prompt, and approve file edits when it asks. |
| Codex | `git clone https://github.com/principalwp/wceh-office-bot.git` then `codex --cd wceh-office-bot`. |
| Claude (claude.ai or Claude Desktop chat) | Settings > Capabilities, turn on "Code execution and file creation" (newer layouts call it "Create and edit files"). Then Customize > Skills > + > Create skill > Upload a skill, and upload the zip without unzipping it: [wceh-office-bot.zip](https://github.com/principalwp/wceh-office-bot/raw/main/wceh-office-bot.zip). If Safari already unzipped a download, right-click the folder, choose Compress, and upload the new zip. |
| ChatGPT | In a Business, Enterprise or Edu workspace: Plugins > Skills > Create > Upload from your computer, and upload the zip: [wceh-office-bot.zip](https://github.com/principalwp/wceh-office-bot/raw/main/wceh-office-bot.zip). On Free, Go, Plus or Pro, use the paste route below with [wceh-office-bot](https://raw.githubusercontent.com/principalwp/wceh-office-bot/main/.agents/skills/wceh-office-bot/SKILL.md). |
| Gemini (gemini.google.com or the Mac app) | Settings > Skills > Create > Upload, with the zip: [wceh-office-bot.zip](https://github.com/principalwp/wceh-office-bot/raw/main/wceh-office-bot.zip). Needs a personal Google account, 18 or older, with Keep Activity on. |
| Grok (grok.com) | Upload the zip as a skill: [wceh-office-bot.zip](https://github.com/principalwp/wceh-office-bot/raw/main/wceh-office-bot.zip). If Grok won't take a zip, use the paste route below. |
| No skill upload in your tool or plan | Paste route: open the raw [wceh-office-bot](https://raw.githubusercontent.com/principalwp/wceh-office-bot/main/.agents/skills/wceh-office-bot/SKILL.md) link, copy all of the text, and paste it into a new conversation with "Follow these instructions for this conversation." Use that conversation for Exercise 2. |

Done when the finished bot shows in your tool (paste route: when the AI answers your paste). To check in Claude Code or Codex, ask "which skills can you use?" and look for its name. If a skill doesn't show, start a new session or conversation.

## Exercise 2: Run the finished bot

`wceh-office-bot: Help me plan out my garden this year.`

Or: `wceh-office-bot: pick three perennials for a sunny front yard in Ottawa`

Answer its questions and approve the plan.

Done when you see the result, the report and the proposed skill updates. If the run is still going when the room moves on, stop it and start Exercise 3.

## Exercise 3: Fill in the Researcher

Open the starter's raw text: [wceh-office-bot-starter/SKILL.md](https://raw.githubusercontent.com/principalwp/wceh-office-bot/main/.claude/skills/wceh-office-bot-starter/SKILL.md). Copy all of it. Coding tools: start a new session in the same folder, and tell it which file to edit: `.claude/skills/wceh-office-bot-starter/SKILL.md` in Claude Code (approve the edit when it asks) or `.agents/skills/wceh-office-bot-starter/SKILL.md` in Codex. Chat tools: start a new conversation. Paste the text, then paste this under it:

`Ask me a bunch of questions to help me create a researcher agent that helps me achieve my goals`

Answer its questions from how you would want it done. Stay in this session or conversation for Exercises 4 to 7.

Done when the Researcher has no TODO left.

## Exercises 4 to 7: Planner, Implementer, Reviewer, Learn (at your own pace)

Stay in the same conversation. For each one, paste its prompt below and answer its questions.

**Exercise 4: Planner.** `Now help me fill in the Planner. Ask me up to 3 questions about how it should plan, then write its Inputs, Instructions, Output and Done when. Write it yourself; don't copy the finished bot.`

Done when the Planner has no TODO left. Compare: [Planner in the finished bot](https://github.com/principalwp/wceh-office-bot/blob/main/.claude/skills/wceh-office-bot/SKILL.md#planner).

**Exercise 5: Implementer.** `Now help me fill in the Implementer. Ask me up to 3 questions about how it should do the work, then write its Inputs, Instructions, Output and Done when. Write it yourself; don't copy the finished bot.`

Done when the Implementer has no TODO left. Compare: [Implementer in the finished bot](https://github.com/principalwp/wceh-office-bot/blob/main/.claude/skills/wceh-office-bot/SKILL.md#implementer).

**Exercise 6: Reviewer.** `Now help me fill in the Reviewer. Ask me up to 3 questions about what it should check, then write its Inputs, Instructions, Output and Done when. Write it yourself; don't copy the finished bot.`

Done when the Reviewer has no TODO left. Compare: [Reviewer in the finished bot](https://github.com/principalwp/wceh-office-bot/blob/main/.claude/skills/wceh-office-bot/SKILL.md#reviewer).

**Exercise 7: Learn.** `Now help me fill in the Learn. Ask me up to 3 questions about what skill updates it should propose, then write its Inputs, Instructions, Output and Done when. Write it yourself; don't copy the finished bot.`

Done when Learn has no TODO left. Compare: [Learn in the finished bot](https://github.com/principalwp/wceh-office-bot/blob/main/.claude/skills/wceh-office-bot/SKILL.md#learn).

When Exercise 7 is done, say `give me my bot`. Chat tools: upload the zip you get back as a skill. If your tool has no upload, save the text as `SKILL.md`. Coding tools: ask it to save the file over `.claude/skills/wceh-office-bot-starter/SKILL.md` (Claude Code) or `.agents/skills/wceh-office-bot-starter/SKILL.md` (Codex), then start a new session. Then run it: `wceh-office-bot-starter: Help me plan out my garden this year.`

## Exercise 8 (stretch): make it yours

Paste: `Now help me fill in the Rules for my own work. Ask me 3 questions about how I work and what I check, then write them.` In Claude Code, write money as `1,000 dollars`, not `$1,000`: Claude Code reads `$1` in a skill as a placeholder and replaces it. Then run it on a real task.

If you have no task in mind, pick one:

- a grant application from past applications and the funder's current guidelines;
- a quarterly board report from this quarter's approved figures only;
- an employee handbook update from current policies and a new regulation;
- a client onboarding pack from the current SOP and templates.

## Writing instructions

1. Say when to read something, such as "read the research before you plan."
2. Give every step a "done when".
3. Say what to do instead of stacking don'ts.
4. Keep each rule in one place.
5. Cut any line that doesn't change what the AI does.

## About

Built for WordCamp Canada 2026 by Stéphane Boisvert ([Principal WP](https://principalwp.com)) and Mikey Arce. Released under the MIT license; see `LICENSE`.
