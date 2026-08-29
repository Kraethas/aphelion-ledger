# Aphelion Ledger

**Time tracking for locked-down laptops.** One HTML file. No install, no account, no network — nothing ever leaves your machine.

If your work computer won't let you install software or sign into a cloud service, most time trackers are simply unavailable to you, and you end up in a spreadsheet. Aphelion Ledger is built for exactly that situation: download one file, double-click it, and start tracking.

[**Download the latest release →**](https://github.com/Kraethas/aphelion-ledger/releases/latest)

<!-- TODO: add a screenshot here once captured, e.g. ![Aphelion Ledger](docs/screenshot.png) -->

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

**Projects** carry a person and department they're for, a status (Not Started, In Development, Completed, Recurring Maintenance), a description, and any number of milestones with due dates that flag amber in their final week and red once overdue.

**Tasks** live inside projects and each has:

- Its own **start/stop timer**. Only one runs at a time, so time can't be double-counted, and a running timer survives closing the browser.
- A **type of work** — meeting/call, development, presentation & e-mail prep, research, documentation, review/QA, planning, support, training, admin, travel.
- A **status** — Not Started, In Progress, Waiting on Other Person/Team, In Review / Approval, Paused, Completed, Cancelled.
- An **assignment** to someone from the container's member list, for tracking who's holding a task and where you're waiting on an answer.
- A **start date and due date**, with the same amber/red flagging.
- **Manual time entry** for work done away from the timer, and a per-task session log so you can delete a timer you left running overnight.

**Members** are the people you can assign tasks to, kept per container. Name is required; team and e-mail are optional. Purely labels for your own tracking — nothing is shared and no e-mail is ever sent.

**Reports** open with what's due: counts of overdue, due today, due this week, and due within 14 days, followed by the tasks themselves grouped by how soon they land. Below that, time logged by project, by type of work, and by department, over a period you choose — with **CSV export** that opens straight in Excel.

## Your data

Everything is stored in your browser's local storage, on your machine, tied to where the file sits. It survives closing the browser and rebooting. A chip in the header confirms saving is working, and warns you in red if a browser policy is blocking it.

Two things follow from that, and they're worth knowing up front:

- Move the file to a different folder or open it in a different browser and it starts empty. **Pick one home for it and keep it there.**
- Clearing your browser's cookies and site data will erase it.

So use **Backup** — it writes a `.json` file with everything in it. **Restore** reads one back. That's also how you move to a new laptop.

## Requirements

Any current browser — Chrome, Edge, or Firefox. Nothing else.

## Contributing

Issues and pull requests are welcome. It's deliberately a single file with no build step and no dependencies; please keep it that way.

## License

MIT — see [LICENSE](LICENSE). Use it, fork it, modify it, ship it commercially. No warranty.
