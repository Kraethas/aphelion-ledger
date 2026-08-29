# Aphelion Ledger

**Time tracking for locked-down laptops.** One HTML file. No install, no account, no network — nothing ever leaves your machine.

If your work computer won't let you install software or sign into a cloud service, most time trackers are simply unavailable to you, and you end up in a spreadsheet. Aphelion Ledger is built for exactly that situation: download one file, double-click it, and start tracking.

**It also runs tabletop RPG campaigns** — the same file, speaking a different language. There's a full section on that further down.

[**Download the latest release →**](https://github.com/Kraethas/aphelion-ledger/releases/latest)

<!-- TODO: add screenshots here once captured, e.g. ![Aphelion Ledger](docs/screenshot.png) -->

---

## Why it exists

Every good time tracker assumes it can install something or phone home. In regulated and locked-down environments — finance, healthcare, government, legal, defence — neither is allowed. Aphelion Ledger works within those constraints rather than around them:

- **No installer.** It's a single `.html` file. Double-click it.
- **No account, no sign-up, no cloud.** There is nothing to sign into.
- **No network access, ever.** The app makes zero outbound requests. Even the logo is drawn inline rather than loaded. It works with the Wi-Fi off, on a plane, or on an air-gapped machine.
- **No telemetry.** Nobody, including the author, can see your data.
- **No admin rights required.**

## What it does

**Containers** keep separate worlds apart — Work, Personal, or anything you add. Each holds its own projects and its own people.

**Projects** carry a person and department they're for, a status, a description, and milestones with due dates that flag amber in their final week and red once overdue.

**Tasks** live inside projects and each has:

- Its own **start/stop timer**. Only one runs at a time, so time can't be double-counted, and a running timer survives closing the browser.
- A **type of work** — meeting/call, development, presentation & e-mail prep, research, documentation, review/QA, planning, support, training, admin, travel.
- A **status** — Not Started, In Progress, Waiting on Other Person/Team, In Review / Approval, Paused, Completed, Cancelled.
- An **assignment** to someone from the container's member list, for tracking who's holding a task and where you're waiting on an answer.
- A **start date and due date**, with the same amber/red flagging.
- **Manual time entry** for work done away from the timer, and a per-task session log so you can delete a timer you left running overnight.

**Members** are the people you can assign work to, kept per container. Name is required; team and e-mail are optional. Purely labels for your own tracking — nothing is shared and no e-mail is ever sent.

**Reports** open with what's due: counts of overdue, due today, due this week, and due within 14 days, followed by the items themselves grouped by how soon they land. Below that, time logged by project, by type of work, and by department, over a period you choose — with **CSV export** that opens straight in Excel.

## Planner

A weekly planner that sits alongside the tracker rather than replacing it.

- **Week view**, Monday to Sunday, with a live marker on the current time.
- **Drag a task onto a day** to block out time for it. Drag blocks to move them between days, or their bottom edge to resize. Everything snaps to 15 minutes.
- **Click a block** to edit it, remove it, or start its timer.
- **Import an `.ics`** exported from Outlook and its meetings become blocks — read straight from your disk, nothing uploaded. All-day and repeating events are skipped and reported rather than dropped silently.
- **Other containers show through greyed out**, read-only and free to overlap, so a day reads as your whole day.

**Planned time is never tracked time.** Blocking two hours logs nothing — only timers and manual entries do. The one bridge is *Start timer* on a planned block. The header shows planned against logged for the week.

## Printable records

**Export record** produces a filing-quality PDF — for your own reference, or for showing someone.

- A single **day in portrait**, or a whole **week in landscape**.
- A graphical timeline drawing your **actual logged sessions** as solid blocks, with planned blocks optionally behind them as dashed outlines.
- An optional **detail page** listing every session — task, project, type, started, stopped, duration, hours — with per-day and grand totals.

It prints through your browser, so *Save as PDF* files it. Nothing leaves your machine.

## Documents

Point a project at a folder on your disk and attach files to the project, to any task, or to any milestone. The file is **copied** into a tidy sub-folder and Ledger keeps a link to the copy:

```
<your folder>/                      project-level documents
<your folder>/Tasks/<task name>/    per task
<your folder>/Milestones/<label>/   per milestone
```

Your originals are never moved. A name clash is saved as `name (2).ext` rather than overwriting. Removing a document removes only Ledger's link — **your files are never deleted.**

> Documents need the File System Access API: **Chrome or Edge on the desktop**. It works from the file itself, no server needed. Firefox and Safari don't offer it, and the app says so plainly instead of half-working. Everything else works in any browser.

---

## It also runs campaigns

Set a container to **Roleplay** instead of Work — when you create it, or later from its settings — and the whole vocabulary follows:

| Work | Roleplay |
| --- | --- |
| Project | **Campaign** |
| Task | **Session** |
| Milestone | **Plot arc** |
| Member | **Player** |
| Person / requester | **Game Master** |
| Department | **System** |
| Due date | **Session date** |

Everything above still works — timers, planner, reports, printable records — it just speaks the right language.

- **Session statuses** — Scheduled, Confirmed, Awaiting Players, Prepped, Played, Postponed, Cancelled.
- **Activities separate prep from play** — GM Prep, Worldbuilding, Maps & Assets, Rules Reading and Recap & Notes sit apart from Live Session, so Reports answers what a session actually costs you.
- **Plot arcs link to sessions, many to many.** A session can belong to several arcs. Click an arc to see every session in it and the hours logged against it.
- **A cast per campaign.** Characters belong to the campaign, not the player — so one person can play several characters, and be someone else entirely in your other campaign. Each is Active, Retired or **Deceased**. Click a player to see every character they've played.
- **Attendance** per session, rolled up per player. Percentages count only sessions marked *Played*, so a scheduled session is never a no-show.
- **A campaign log** — a third export option that prints one campaign as a chronological record: the cast with attendance, the arcs with time against each, and every session with its date, activity, arcs, who was present and how long it ran.
- **Documents** file under `Sessions/` and `Plot arcs/` instead.

Switching a container between modes re-maps statuses and activities by position, and switching back restores them. Names, notes, dates, arc links, cast and logged time are never touched.

---

## Your data

Everything is stored in your browser's local storage, on your machine, tied to where the file sits. It survives closing the browser and rebooting. A chip in the header confirms saving is working, and warns you in red if a browser policy is blocking it.

Two things follow from that, and they're worth knowing up front:

- Move the file to a different folder or open it in a different browser and it starts empty. **Pick one home for it and keep it there.**
- Clearing your browser's cookies and site data will erase it.

So use **Backup** — it writes a `.json` file with everything in it. **Restore** reads one back. That's also how you move to a new laptop.

## Requirements

Any current browser — Chrome, Edge, or Firefox. Nothing else. (Documents alone need Chrome or Edge, as noted above.)

## Support it

Ledger is free and always will be. If it saves you a spreadsheet or earns a place at your table, there's a tip jar at **[ko-fi.com/kraethas](https://ko-fi.com/kraethas)**.

## Contributing

Issues and pull requests are welcome. It's deliberately a single file with no build step and no dependencies; please keep it that way.

## License

MIT — see [LICENSE](LICENSE). Use it, fork it, modify it, ship it commercially. No warranty.
