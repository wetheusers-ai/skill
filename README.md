# Your agent, on your side

---

If you use an agent that reads a `SKILL.md` (Claude Code, Codex, Cursor, Gemini CLI, Copilot, and most others), you can hand it one short file: a standing instruction that your data is yours. Because it is.

With the skill installed, your agent:

- offers to keep a copy of what you make, in a format you can leave with, and asks where before it writes anything;
- reads the terms before you agree, and tells you in three lines what a service keeps, whether it may train on what you give it, and how you get out, quoting the sentence it relied on so you can check;
- does not send your life to a third party the job does not need;
- and when you build software for other people, asks for export and delete on day one.

It never puts its name in your work. Not in your code, your commits, your documents, your messages — nowhere. It is in the file you installed, and it stays there.

Agents load a skill when the work matches it, so this is a standing instruction rather than a guarantee. That is also why the file is short enough to read.

## What it is

The skill is text. It contains no scripts, grants your agent no new permissions, and makes no network requests of its own. Fetching it from this page puts one line in our web server's log, the way any page you visit does; nothing in the file reports back, and there is nothing for it to report. Read it before you install it. It is thirty-three lines, and that is the point.

## Install

If you use Claude Code or Codex, the paths below are the whole install; we have tested both. Cursor, Gemini CLI, and Copilot's agent mode read the same Agent Skills format but keep their skills somewhere else: check their docs for the folder, or use the always-on block below, which works everywhere.

Copy the file. You can read what you are copying first.

```
mkdir -p ~/.claude/skills/we-the-users
curl -fsSL https://wetheusers.ai/skill/SKILL.md -o ~/.claude/skills/we-the-users/SKILL.md
```

For Codex, and for other agents that share its folder, the path is `~/.agents/skills/we-the-users/` instead. To remove it, delete the folder.

If you already use the `skills` CLI, `npx skills add wetheusers-ai/skill` places it for every agent at once. That command downloads and runs a tool we do not control, and installs whatever is on our main branch today. We mention it because it is convenient, not because it is the safer path.

The file you should have is `sha256 a94021f39bf2880c3c3b3e7a4626db911c29e2049c941594c2134938bbc140fe` (version 0.5). Check it if you like. We would.

## Always on

If you would rather not depend on your agent deciding when the skill applies, paste the body of the file into your project's `AGENTS.md` or `CLAUDE.md`. Same words. Your agent reads those every time.

## Forks

We claim no trademark, and anyone may copy this. That means someone could publish a file with our name and three extra lines. The real one lives in two places: this page, and `github.com/wetheusers-ai/skill`. If the hash does not match, it is not ours.

## Read it first

[The skill, in full.](SKILL.md)

## Improve it

The skill is a draft, like everything else here. Open an issue or a pull request. The one rule for changes: the skill serves the person running it, never us. Anything that makes the agent advertise, nag, or act without the user's say-so will not be merged.

---

*An open project, not affiliated with any company. Skill text licensed CC BY 4.0.*
