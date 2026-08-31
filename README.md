# Aphelion Ledger

**One HTML file that keeps an honest record of where your time and money went.** No install, no account, no network — nothing ever leaves your machine.

It does two jobs with the same machinery. Set a container to **Work** and it tracks projects, tasks and invoices. Set it to **Roleplay** and it tracks campaigns, sessions, plot arcs and who was at the table. You can run both side by side.

[**Download the latest release →**](https://github.com/Kraethas/aphelion-ledger/releases/latest)

<!-- TODO: add screenshots here once captured, e.g. ![Aphelion Ledger](docs/screenshot.png) -->

---

## Why it works this way

Every good tracker assumes it can install something or phone home. On a locked-down work laptop — finance, healthcare, government, legal, defence — neither is allowed, so people end up in a spreadsheet they resent. Aphelion Ledger is built to survive those constraints rather than route around them:

- **No installer.** A single `.html` file. Double-click it.
- **No account, no cloud, no sync.** There is nothing to sign into.
- **No network access, ever.** Zero outbound requests — even the logo is drawn in code rather than loaded. It works with the Wi-Fi off, on a plane, or on an air-gapped machine.
- **No telemetry.** Nobody, including the author, can see your data.
- **No admin rights.**

The first time you open it, it asks what you're tracking and sets itself up accordingly. You can change that any time from the **⚙** button in the header.

## The shape of it

**Containers** are separate worlds — *Work*, *Personal*, *My Campaigns*. Each holds its own projects, its own people, its own planner and its own currency. Each is either a Work container or a Roleplay one.

**Projects** (*Campaigns*) hold the work. **Tasks** (*Sessions*) hold the doing. **Milestones** (*Plot arcs*) mark the shape of it.

## Tracking time

Every task has its own **start/stop timer**. Only one runs at a time, so time can never be double-counted, and a running timer survives closing the browser — it keeps counting until you stop it.

- A **type of work** on every task, so you can answer *where did the week actually go*.
- A **status**: Not Started, In Progress, Waiting on Other Person/Team, In Review / Approval, Paused, Completed, Cancelled.
- An **assignment** to someone from the container's member list — useful mainly for seeing who owes you an answer.
- **Start and due dates**, which turn amber in their final week and red once overdue.
- **Manual entry** for work done away from the timer, and a session log so you can delete the timer you left running overnight.

## Tracking money

Every task has an optional **Cost**. Leave it blank and money never appears; fill it in and it rolls into the project total, Reports, the CSV and the printed record. Currency is per container.

Work projects can also keep **bills and balances** — a *one-off bill* you pay down to zero, or a *running balance* that new charges add to, like a card. Payments and charges are ordinary tasks using the **Payment** and **Charge** types, pointed at an account, so they carry dates, notes and documents like anything else.

Two rules keep the numbers trustworthy:

- **Balances are derived, never stored.** Outstanding is recalculated from the payments themselves, so editing or deleting one corrects the balance immediately and it can never drift.
- **Spent and Still owed are never added together.** Spend is cash basis — counted when money actually leaves — so a charge raises what you owe but isn't spend until you pay it. The CSV marks every cost *counts as spend* yes or no, so the distinction survives into Excel.

## Planning the week

The **Planner** is a companion to the tracking, not a replacement for it.

- A **week view**, Monday to Sunday, with a live marker on the current time.
- **Drag a task onto a day** to block out time. Drag blocks between days, or their bottom edge to resize. Everything snaps to 15 minutes.
- **Click a block** to edit it, delete it, or start its timer.
- **Import an `.ics`** from Outlook and its meetings become blocks, read straight off your disk. All-day and repeating events are skipped and counted for you rather than dropped silently.
- Blocks from your **other containers** show through greyed out and read-only, so a day reads as your whole day without mixing the containers together.

**Planned time is never tracked time.** Blocking two hours logs nothing — only timers and manual entries do. The header shows planned against logged, which is the point: you can see where the plan and the week parted company.

## Reports

Reports open with **what's due** — overdue, today, this week, the next 14 days — then time by project, by type of work and by department for a period you choose, then **money**: spent in the period, still owed, and where it went.

**CSV export** opens straight in Excel, with a separate costs block after the time rows.

## Printable records

**Export record** produces something you can file or hand to someone: a **day in portrait** or a **week in landscape**, drawn as a timeline of the hours you actually logged, optionally with your plan behind it as dashed outlines, and an optional detail page itemising every session and cost.

Roleplay containers get a third option — a **campaign log**: the cast with each player's attendance, the plot arcs with time against each, and every session with its date, activity, who was present and how long it ran.

It prints through your browser, so *Save as PDF* files it.

## Documents

Point a project at a folder on your disk and attach files to the project, to any task, or to any milestone. The file is **copied** into a tidy sub-folder and Ledger keeps a link to the copy:

```
<your folder>/                      project-level documents
<your folder>/Tasks/<task name>/    per task      → Sessions/ in roleplay
<your folder>/Milestones/<label>/   per milestone → Plot arcs/ in roleplay
```

Your originals are never moved. A name clash saves as `name (2).ext` rather than overwriting. Removing a document removes only Ledger's link — **your files are never deleted.**

> Documents need the File System Access API, which means **Chrome or Edge on the desktop**. It works from the file itself; no server needed. Firefox and Safari don't offer it, and the app says so plainly rather than half-working. Everything else works in any browser.

## Sharing, one writer and many readers

The people icon in the header turns on a **shared folder** mode: you publish, other people read. It needs a folder everyone can reach (OneDrive, SharePoint, any synced folder) and Chrome or Edge.

- **Publishing** — Ledger writes a snapshot of your visible containers into the folder a few seconds after every change.
- **Viewing** — Ledger reads someone else's snapshot and shows it read-only, re-checking every minute.

**What viewers see is per container.** A container's settings has *Visible to viewers*; anything left off is **never written to the shared file at all**. It doesn't leave your machine. In a folder other people can open, absence is the only real way to hide something.

Two things this deliberately is not:

- **Not access control.** Anyone who can open the folder can read the published file directly, whatever Ledger shows them. The folder's sharing list is the real boundary.
- **Not collaboration.** Only the owner writes. Viewers can't log their own time.

If you also use Ledger yourself, viewing someone else's is safe: while viewing, it never writes to your own stored data.

## Filters

Every data table — tasks, cast, members, what's due, report detail — has a filter row under its headings. Dropdowns for columns with a fixed set of values, listing only what's actually present so no choice is a dead end; free text for names and titles. Filters stack, and a bar reads *Showing 8 of 16 · Clear filters* whenever anything is hidden, so a filtered list is never mistaken for missing data.

---

## Roleplay mode

Set a container to **Roleplay** and the vocabulary follows:

| Work | Roleplay |
| --- | --- |
| Project | **Campaign** |
| Task | **Session** |
| Milestone | **Plot arc** |
| Member | **Player** |
| Person / requester | **Game Master** |
| Department | **System** |
| Due date | **Session date** |

Everything above still works. What roleplay adds:

- **Session statuses** — Scheduled, Confirmed, Awaiting Players, Prepped, Played, Postponed, Cancelled.
- **Activities separate prep from play** — GM Prep, Worldbuilding, Maps & Assets, Rules Reading and Recap & Notes sit apart from Live Session, so Reports answers what a session really costs you.
- **Plot arcs link to sessions, many to many.** Click an arc to see every session in it and the hours against it.
- **A cast per campaign.** Characters belong to the campaign rather than the player, so one person can play several characters and be someone else entirely in your other campaign. Each is Active, Retired or **Deceased**. Click a player to see everyone they've played.
- **Attendance** per session, rolled up per player and per campaign. Percentages count only sessions marked *Played*, so a scheduled session is never a no-show.
- **Campaign cost** as an activity type, for a VTT licence or a rulebook. Campaigns get the Cost field but not accounts — a table's spending is one-off rather than a balance.

Switching a container between modes re-maps statuses and activities by position, and switching back restores them. Names, notes, dates, arc links, cast and logged time are never touched.

---

## Your data

Everything lives in your browser's local storage, on your machine, tied to where the file sits. It survives closing the browser and rebooting. A chip in the header confirms saving works, and turns red if a browser policy is blocking it.

Two consequences worth knowing before you rely on it:

- Move the file to a different folder, or open it in a different browser, and it starts empty. **Pick one home for it and keep it there.**
- Clearing your browser's cookies and site data erases it.

So use **Backup** — it writes a `.json` file with everything in it, and **Restore** reads one back. That's also how you move to a new laptop. Restore replaces everything, so back up first.

## Requirements

Any current browser — Chrome, Edge or Firefox. Documents alone need Chrome or Edge.

## Support it

Ledger is free and always will be. If it saves you a spreadsheet or earns a place at your table, there's a tip jar at **[ko-fi.com/kraethas](https://ko-fi.com/kraethas)**.

## Contributing

Issues and pull requests welcome. It is deliberately one file with no build step and no dependencies — please keep it that way.

## License

MIT — see [LICENSE](LICENSE). Use it, fork it, modify it, ship it commercially. No warranty.
