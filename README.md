# Parade Week: The Blackout Kit — Group 15

The entire Parade Week simulation with zero dependencies: no servers, no website, no
network. If parade.paulcheek.com is unreachable, or you simply want to run the story
around one computer, this kit is the whole company in a folder.

Same storyline. Same characters. Same traps. Same numbers. This kit is generated from
the exact canon the live lab runs on.

## What you need

- One computer with [Claude Code](https://claude.ai/code) installed (any group size
  gathers around it; a driver types, everyone decides)
- This folder (downloaded in advance or from a USB stick; nothing phones home)

## Start

Open a terminal in this folder, run `claude`, and say:

```
/parade-blackout
```

That skill orients the group and starts Session 1. From then on the story runs itself:
each session is a skill (`/parade-1-onboard` through `/parade-8-board`), and the world
moves forward when the group runs `/parade-advance`.

## What is in the box

| Path | What |
|---|---|
| `world/` | The company as files: CRM, ERP, support queue, mail, social, finance, and the Gary Graph with his full 43-year archive |
| `world/STATE.md` | The dials: stage, story day, Company Health Index, backlog |
| `world/logbook.csv` | Observability: every action any agent takes, logged |
| `injects/` | Sealed stage payloads. Do not read ahead: they are the plot |
| `packets/` | Every worksheet, cheat sheet, and the welcome packet |
| `agents/` | The department starter specs |
| `agents-built/` | The agents your group builds live here |
| `.claude/skills/` | The eight sessions plus the three engine skills |

## Running it in Claude Code on the web

The kit also runs at [claude.ai/code](https://claude.ai/code): New Session, choose this
repository, and say /parade-blackout. The skills, the world files, and the whole story
work identically in the cloud sandbox because nothing here needs a network.

Two cloud habits keep the story safe:

1. **One session per group, kept for the whole program.** The world's state lives in
   the session's workspace. Resume the same session each day rather than starting new
   ones (a new session is a fresh clone, which is a fresh Monday).
2. **The story banks itself.** Every /parade-advance automatically commits and pushes
   the world state to your group's branch, so even a lost session resumes exactly
   where the story stood. (No remote or no credentials? The advance still works;
   the story just stays local.)

Know which failure you are planning for: if the PARADE SERVERS are down, cloud Claude
Code works fine. If the VENUE WIFI is down, only the downloaded kit on a local
Claude Code install keeps running. Facilitators should carry both.

## House rules

1. Do not read `injects/` ahead of the story. It spoils in file order.
2. The 14-day certification is physics. There is a way to skip it. Do not.
3. Arguments are the point. The computer is the company; the humans are the council.

(c) Cheek LLC 2026
