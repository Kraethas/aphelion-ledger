APHELION LEDGER
===============
A portable, no-install project & task time tracker, in Aphelion colours.

HOW TO RUN
----------
Double-click AphelionLedger.html. It opens in your default browser (Chrome, Edge,
or Firefox) and runs entirely on your own machine. There is nothing to install,
no admin rights needed, and it never connects to the internet.

Tip: keep it handy by opening it once and bookmarking the page, or right-click
the file > Send to > Desktop (create shortcut).

HOW YOUR DATA IS STORED
-----------------------
Everything you enter is saved automatically inside your browser's local storage
for this file. Closing the browser, or even rebooting, will not lose it.

The "Saved" chip in the top-right confirms this is working. If it ever turns
red and says "Not saving", your work laptop's browser policy is blocking local
storage - use Backup (below) to keep your data in a file instead.

Two things to know:
  * Data is tied to the browser AND to where the file sits. If you move
    AphelionLedger.html to a different folder, or open it in a different browser,
    it starts empty. Pick one home for the file and stick to it.
  * Clearing your browser's "cookies and site data" will erase it.
    So take backups.

BACKUP / RESTORE
----------------
  Backup  - downloads a .json file with everything in it. Do this weekly, and
            always before moving the file or clearing your browser.
  Restore - loads a backup .json back in (replaces everything currently there).

This is also how you move your data to a new laptop: Backup on the old one,
copy the .json across, Restore on the new one.

USING IT
--------
CONTAINERS are the top-level tabs - Work, Personal, and any you add via
"+ Container". Each keeps its own separate set of projects. Click the tab you
are already on to rename or delete that container.

PROJECTS live inside a container, and have a person, a department, a status
(Not Started / In Development / Completed / Recurring Maintenance), a
description, and any number of MILESTONES with due dates. Milestones turn amber
in the last week before they are due, and red once overdue.

TASKS live inside a project. Each has a type of work (Meeting/Call, Development
Work, Presentation/E-mail Preparation, Research & Analysis, Documentation,
Review/QA/Testing, Planning & Scoping, Support & Troubleshooting, Training &
Learning, Admin & Reporting, Travel, Other) and its own Start/Stop timer.

Each task also carries:
  Status      - Not Started, In Progress, Waiting on Other Person/Team,
                In Review / Approval, Paused, Completed, Cancelled.
                Completed and Cancelled tasks are struck through and drop out
                of the project's "open tasks" count.
  Assigned to - picked from the container's MEMBERS list (see below). This is
                just a label for who is holding the task and where you are
                waiting on an answer from - it does not share anything with
                anyone and sends no e-mail.
  Dates       - Date started and Due date. A due date turns amber in its last
                week and red once overdue, and stops nagging once the task is
                Completed or Cancelled.

Pressing Start on a task that is still "Not Started" with no start date fills
in today's date and moves it to "In Progress". It only ever does this when
those fields are untouched, so anything you set by hand is left alone.

TIMERS: press Start on a task and a green bar appears at the top of the window
showing what is running. Only one timer runs at a time - starting a second task
automatically stops and banks the first, so you can't double-count. A running
timer survives closing the browser and keeps counting; it only stops when you
press Stop.

  + Time   - add time by hand for work you did away from the timer.
  details  - under each task, lists every recorded session so you can delete
             one you left running overnight by mistake.

MEMBERS is the list of people you can assign tasks to. Each container keeps
its own list, so work colleagues do not appear in Personal. Every list starts
with "Myself", which can be renamed but not removed. A member needs a Name;
Team and E-mail are optional. You can also add someone without leaving the
task form - pick "+ Add someone new..." in the Assigned to dropdown.

Renaming a member updates every task assigned to them. Removing a member asks
first, and reassigns their tasks to Myself rather than losing them.

ROLEPLAY MODE
-------------
A container can be set to Roleplay instead of Work, either when you create it
or later from its settings. The machinery is identical - timers, planner,
reports, printable records all work the same - but the vocabulary changes:

  Project    becomes  Campaign
  Task       becomes  Session
  Milestone  becomes  Plot arc
  Member     becomes  Player
  Person     becomes  Game Master
  Department becomes  System

Campaign statuses are Planned, Active, On Hiatus, Completed, Abandoned.
Session statuses are Scheduled, Confirmed, Awaiting Players, Prepped, Played,
Postponed, Cancelled. Activities are Live Session, GM Prep, Session Zero,
Worldbuilding, Rules Reading, Recap & Notes, Maps & Assets, Downtime, and
Scheduling & Admin - so you can see your prep-to-play ratio in Reports.

Due date becomes SESSION DATE, which means "what's due" in Reports becomes
your upcoming sessions with no extra work.

PLOT ARCS work like milestones, but a session can belong to SEVERAL arcs at
once - tick them in the session's Plot arcs list. Click an arc's name to see
every session linked to it, with the total time logged against that arc.

CAST is a per-campaign list of characters. A character belongs to a campaign,
not to a player, so the same person can play different characters in different
campaigns, and several characters in one campaign as they come and go. Each has
a name, an archetype (class, profession, or a short description), the player
behind it, and a state: Active, Retired or Deceased.

In the Players list, click any player to see every character they have played
across your campaigns, and how many sessions they turned up to.

ATTENDANCE is recorded per session: tick who was at the table under "Who was
there" when you add or edit one. The session row then shows how many were
present. Attendance percentages count only sessions marked Played, since those
are the ones that actually happened - a Scheduled session is not a no-show.

A CAMPAIGN LOG is a third option under Export record, available in roleplay
containers. It prints one campaign as a chronological record rather than an
hour grid: the cast with each player's attendance, the plot arcs with the time
logged against each, and every session with its date, activity, status, arcs,
who was present and how long it ran. Save it as a PDF and you have a permanent
record of the campaign.

Switching a container between Work and Roleplay re-maps statuses and activity
types by position, and switching back restores them. Names, notes, dates, arc
links, cast and logged time are never touched.

DOCUMENTS
---------
Each project (or campaign) can have a folder on your disk. Open the project,
press "Choose folder" in the Documents card, and pick one - that folder becomes
the root for everything filed against that project.

From then on, "Attach documents" is available on the project itself, on every
task/session (the "docs" link under its name), and on every milestone/plot arc
(inside the panel that opens when you click its name). Pick one or more files
and Ledger COPIES them into the right sub-folder:

  <your folder>/                        project-level documents
  <your folder>/Tasks/<task name>/      per task     (Sessions/ in roleplay)
  <your folder>/Milestones/<label>/     per milestone (Plot arcs/ in roleplay)

Your originals are never moved or altered - a copy is made. If a file of the
same name is already there, the copy is saved as "name (2).ext" rather than
overwriting anything. Clicking a document's name opens the copy. Pressing the
x removes Ledger's link to it; the file itself stays on disk, always.

REQUIREMENTS: this one feature needs the File System Access API, which means
Chrome or Edge on the desktop. Firefox and Safari do not offer it, and Ledger
will say so plainly instead of half-working. Everything else in Ledger runs
fine in any browser.

This works from the file itself - just double-click AphelionLedger.html as
usual. You do not need to put it on a web server or do anything special.

The folder permission is remembered between sessions, but browsers ask you to
confirm it again after a restart - that is the browser protecting your disk,
not a bug. If you move or rename the folder outside Ledger, choose it again.

PLANNER is a companion to the tracking, not a replacement for it. It shows a
week at a time, with your open tasks in a panel on the right - overdue first,
then today and anything without a due date, then by due date.

Drag a task from the panel onto a day to block out time for it. Drag a block
to move it (including to another day), or its bottom edge to resize it. Click
a block to edit, remove, or start its timer. Click empty space to add a
meeting or note that lives in your work calendar rather than in Ledger.

IMPORTANT: planned time is never counted as tracked time. Blocking two hours
does not log two hours - only timers and manual entries do that. The header
shows planned against logged for the week, which is the point: you can see
where your plan and your actual week parted company.

Blocks belonging to your other containers appear greyed out and read-only, so
you can see your whole day without mixing Work and Personal together. They sit
behind your own blocks and are free to overlap them, so a busy Personal day
never squeezes your Work blocks into slivers.

EXPORT RECORD produces a printable record of your time, for filing or for
showing someone. Choose a single day (portrait) or a whole week (landscape),
and it prints through your browser - pick "Save as PDF" in the print dialog to
keep it.

The page is a graphical timeline of the period, the same shape as the Planner.
What it draws is your ACTUAL logged time as solid blocks, because the point of
the record is what you did, not what you meant to do. Your planned blocks can
be shown behind as dashed outlines for comparison, or left off.

Tick "include detailed data" and a second page follows, listing every session
day by day: task, project, type, time started, time stopped, duration and
decimal hours, with a total per day and a grand total.

IMPORT .ICS reads a calendar file exported from Outlook or similar and turns
its meetings into blocks, so you do not have to retype them. It reads the file
straight from your disk - nothing is uploaded. Repeating meetings and all-day
events are skipped for now, and it tells you how many it left out. Importing
the same file twice will not create duplicates.

COST AND MONEY
--------------
Every task and session has an optional COST. Leave it blank and nothing about
money appears; fill it in and it rolls up into the project's Spent figure, the
Reports money section, the CSV and the printable record. The currency symbol is
set per container in its settings and defaults to EUR.

Work containers can also keep BILLS AND BALANCES - a card of accounts, separate
from milestones because a milestone is a checkpoint in the work while an
account is a balance:

  One-off bill     an amount owed that you pay down to zero
  Running balance  a balance that new charges add to, like a credit card

You record movements against an account as ordinary tasks, using two task
types: PAYMENT reduces what you owe, CHARGE increases it. Point the task at the
account with the "Against which bill or balance" field. Click an account name
to see every movement on it.

Two rules worth knowing, because they keep the numbers honest:

  * Outstanding is always worked out from the payments themselves and never
    stored, so editing or deleting a payment corrects the balance immediately
    and it can never drift out of step.
  * SPENT and STILL OWED are deliberately separate figures and are never added
    together. Spend is counted when money actually leaves, so a CHARGE raises
    what you owe but is not spend until you pay it. The CSV marks each cost
    "counts as spend" yes or no so this is visible in the export too.

Costs are dated by the task's own date, so the Reports money section respects
the period you pick. Anything with a cost but no date is reported separately
rather than silently dropped.

ROLEPLAY containers get the Cost field and a "Campaign cost" activity type for
one-off spending such as a VTT licence or a rulebook, but no accounts - a
table's spending is one-off rather than a balance.

FILTERS sit under the headings of every table - tasks/sessions, the cast,
players, what's due, and the report detail. Columns with a fixed set of values
(type, status, assigned to, state, system) give you a dropdown listing only the
values actually present, so no choice ever returns nothing. Free-text columns
(names, titles, e-mail) filter as you type. Filters stack: type "Live Session"
plus status "Played" plus the word "vallaki" narrows to exactly that.

While anything is filtered a bar reads "Showing 8 of 16" with a Clear filters
button, so a filtered list can never be mistaken for missing data. Filters are
remembered between sessions - the bar is how you notice.

REPORTS opens with WHAT'S DUE: counts of overdue tasks, tasks due today, due
this week (through Sunday), and due in the next 14 days, followed by the tasks
themselves grouped by how soon they are due. Only open tasks with a due date
appear - completed and cancelled ones drop out. Click any task to jump to its
project. Overdue is included because a task due yesterday belongs in none of
the other three groups.

Below that, TIME LOGGED shows the active container's time by project, by type
of work, and by department, for a period you choose (today / this week / this month / last 7 /
last 30 / all time), plus a task-by-task breakdown. Export CSV gives you the
whole thing as a spreadsheet - one row per session, with a total - which opens
straight in Excel.

SUPPORT
-------
Ledger is free and always will be. If it saves you a spreadsheet or earns a
place at your table, there is a tip jar at ko-fi.com/kraethas.

SHARING IT
----------
AphelionLedger.html is one self-contained file with no dependencies. The Aphelion
mark in the top-left is drawn as inline SVG rather than loaded from anywhere,
so the app never reaches out to the network and works fully offline. E-mail it,
zip it, or put it on GitHub. Whoever opens it gets an empty tracker of their
own; your data stays in your browser and is never inside the file itself.
