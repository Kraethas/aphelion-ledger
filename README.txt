APHELION LEDGER
===============
One HTML file that keeps an honest record of where your time and money went.
No install, no account, no network - nothing ever leaves your machine.

It does two jobs with the same machinery. A container set to Work tracks
projects, tasks and invoices. A container set to Roleplay tracks campaigns,
sessions, plot arcs and who was at the table. You can run both side by side.

Free and open source (MIT). Source and newest version:
  https://github.com/Kraethas/aphelion-ledger


HOW TO RUN
----------
Double-click AphelionLedger.html. It opens in your default browser and works.
There is nothing to install, no admin rights needed, and it never connects to
the internet.

The first time you open it, it asks what you are tracking and sets itself up
accordingly. You can change that later with the gear button in the header.

Tip: open it once and bookmark the page, or right-click the file and choose
Send to > Desktop (create shortcut).


WHERE YOUR DATA LIVES
---------------------
Everything you enter is saved automatically in your browser's local storage
for this file. Closing the browser, or rebooting, will not lose it. The
"Saved" chip in the header confirms this is working; if it turns red, a
browser policy is blocking storage and you should rely on Backup instead.

Two consequences worth knowing before you rely on it:

  * Data is tied to the browser AND to where the file sits. Move the file to
    a different folder, or open it in another browser, and it starts empty.
    Pick one home for the file and keep it there.
  * Clearing your browser's "cookies and site data" will erase it.

BACKUP writes a .json file with everything in it. RESTORE reads one back, and
replaces everything currently in the app - so take a Backup first. This is
also how you move your data to a new machine.


THE SHAPE OF IT
---------------
CONTAINERS are separate worlds - Work, Personal, My Campaigns. Each holds its
own projects, its own people, its own planner and its own currency, and each
is either a Work container or a Roleplay one. Click the tab you are already on
to rename it, change what it is for, or delete it.

The project list on the left is in whatever order you put it in. Drag the grip
handle at the left of a row to move it; the order is saved and is the order
used everywhere else, including printed records. Clicking a row still just
selects it.

PROJECTS (Campaigns) hold the work. Each has a person and department it is for
(Game Master and System in roleplay), a status, a description, and MILESTONES
(Plot arcs) with due dates that turn amber in their final week and red once
overdue.

TASKS (Sessions) live inside projects.


TRACKING TIME
-------------
Every task has its own start/stop timer. Only one runs at a time, so time can
never be double-counted, and a running timer survives closing the browser - it
keeps counting until you press Stop.

Each task also carries:

  Type        what kind of work it was, so reports can answer where the week
              went. In roleplay this becomes the Activity, which separates GM
              Prep, Worldbuilding, Maps & Assets and Rules Reading from Live
              Session.
  Status      Not Started, In Progress, Waiting on Other Person/Team,
              In Review / Approval, Paused, Completed, Cancelled, Recurring.
              In roleplay: Scheduled, Confirmed, Awaiting Players, Prepped,
              Played, Postponed, Cancelled, Recurring.

              RECURRING is for standing commitments that never finish - a
              daily stand-up, a weekly steering call, a weekly game. Give it
              no due date and it stays out of What's due instead of nagging
              you every day, while its timer still accumulates every time you
              run it. It is counted separately from open work, so a project
              header reads "5 tasks (2 open . 2 recurring)" rather than
              letting standing items inflate a to-do count that never falls.
  Assigned to someone from the container's member list. A label for your own
              tracking - nothing is shared and no e-mail is ever sent.
  Dates       a start date and a due date (the session date in roleplay).
  Cost        optional; see MONEY below.

  + Time      records work done away from the timer.
  details     lists every recorded session so you can delete one you left
              running overnight.


MONEY
-----
Every task has an optional COST. Leave it blank and nothing about money
appears; fill it in and it rolls up into the project's Spent figure, Reports,
the CSV and the printed record. The currency symbol is set per container.

Work containers can also keep BILLS AND BALANCES:

  One-off bill     an amount owed that you pay down to zero
  Running balance  a balance that new charges add to, like a credit card

Movements are ordinary tasks using two types - PAYMENT reduces what you owe,
CHARGE increases it - pointed at an account with the "Against which bill or
balance" field. Click an account name to see every movement on it.

Two rules keep the numbers trustworthy:

  * Outstanding is worked out from the payments themselves and never stored,
    so editing or deleting a payment corrects the balance immediately and it
    can never drift out of step.
  * SPENT and STILL OWED are separate figures and are never added together.
    Spend is counted when money actually leaves, so a CHARGE raises what you
    owe but is not spend until you pay it. The CSV marks each cost "counts as
    spend" yes or no so this survives the export.

Costs are dated by the task's own date, so the money section respects the
period you pick. Anything with a cost but no date is reported separately
rather than silently dropped.


MINI CONTROL
------------
The stopwatch button in the header opens a small window holding three
dropdowns - container, project, task - and one Start/Stop button. It is for
logging time without hunting for the Ledger tab.

In Chrome and Edge it floats ABOVE your other windows, so it stays visible
while you work in something else. That uses Document Picture-in-Picture, which
is the only way a web page can sit on top; in other browsers it opens as an
ordinary small window instead, which behaves the same but can be covered.

+ NEW TASK lets you name something and start timing it without deciding where
it belongs. Pick "- Unfiled -" as the project and the task is created in an
Unfiled project in that container, which Ledger makes the first time you need
it. Type the name, press Enter, and the clock is running.

FILED UNDER, in a task's edit dialog, is how you put it where it belongs
later. It lists every container and project, and moving a task takes its
logged time with it. Links that only made sense where it came from - plot
arcs, an account, attendance from another container's players - are cleared,
because they do not exist at the destination.

It is the same timer as the main window, not a second one. Starting in either
place shows up in both, and the one-timer-at-a-time rule still applies. Press
the header button again to close it.


PLANNER
-------
A companion to the tracking, not a replacement for it. It shows a week at a
time, with your open tasks in a panel on the right - overdue first, then today
and anything undated, then by due date.

Drag a task from the panel onto a day to block out time. Drag a block to move
it (including to another day), or its bottom edge to resize. Click a block to
edit, remove, or start its timer. Click empty space to add a meeting or note
that lives in your work calendar rather than here.

The LOGGED button puts the time you actually recorded on the same grid. The
plan keeps the left of each day column and your real sessions appear on the
right in green, so you can see where the two agreed and where they did not.
A session still running is outlined rather than filled. Turn it off and the
plan goes back to the full width.

PLANNED TIME IS NEVER TRACKED TIME. Blocking two hours does not log two hours
- only timers and manual entries do. Logged blocks are drawn from your real
sessions and cannot be dragged or edited from here; they are the record, not
the plan. The header shows planned against logged for the week.

Blocks belonging to your other containers appear greyed out and read-only, and
sit behind your own so a busy personal week never squeezes your work blocks
into slivers.

IMPORT .ICS reads a calendar file exported from Outlook and turns its meetings
into blocks. The file is read straight from your disk - nothing is uploaded.
Repeating and all-day events are skipped, and it tells you how many it left
out. Importing the same file twice will not create duplicates.


REPORTS
-------
Reports open with WHAT'S DUE: counts of overdue, due today, due this week and
due within 14 days, then the tasks themselves grouped by how soon they land.
Only open tasks with a date appear. Click any task to jump to its project.

Below that: TIME LOGGED by project, by type of work and by department for a
period you choose, then MONEY - spent in the period, still owed, and where it
went. EXPORT CSV gives you the whole thing as a spreadsheet, with a separate
costs block after the time rows.


PRINTABLE RECORDS
-----------------
EXPORT RECORD produces something you can file or hand to someone. Choose a
single day (portrait) or a whole week (landscape); it prints through your
browser, so pick "Save as PDF" in the print dialog to keep it.

The page is a graphical timeline of the period. What it draws is your ACTUAL
logged time as solid blocks, because the point of a record is what you did,
not what you meant to do. Your planned blocks can sit behind as dashed
outlines for comparison, or be left off. Tick "include detailed data" and a
second page lists every session and cost with per-day and grand totals.

Roleplay containers get a third option, a CAMPAIGN LOG: one campaign as a
chronological record - the cast with each player's attendance, the plot arcs
with the time logged against each, and every session with its date, activity,
arcs, who was present and how long it ran.


DOCUMENTS
---------
Each project can have a folder on your disk. Open it, press "Choose folder" in
the Documents card, and pick one - that becomes the root for everything filed
against that project.

"Attach documents" is then available on the project itself, on every task (the
"docs" link under its name), and on every milestone (inside the panel that
opens when you click its name). Files are COPIED into the right sub-folder:

  <your folder>/                        project-level documents
  <your folder>/Tasks/<task name>/      per task     (Sessions/ in roleplay)
  <your folder>/Milestones/<label>/     per milestone (Plot arcs/ in roleplay)

Your originals are never moved or altered. If a file of the same name is
already there, the copy is saved as "name (2).ext" rather than overwriting
anything. Clicking a document opens the copy. Pressing the x removes Ledger's
link to it; the file itself always stays on disk.

REQUIREMENTS: this one feature needs the File System Access API, which means
Chrome or Edge on the desktop. It works from the file itself - just
double-click as usual, no server needed. Firefox and Safari do not offer it,
and Ledger says so plainly instead of half-working. Everything else in Ledger
runs fine in any browser.

The folder permission is remembered, but browsers ask you to confirm it again
after a restart - that is the browser protecting your disk, not a bug. If you
move or rename the folder outside Ledger, choose it again.


SHARING - ONE WRITER, MANY READERS
----------------------------------
The people icon in the header sets what this copy of Ledger is. Off is the
default and nothing is shared. The other two modes need a folder everyone
involved can reach - OneDrive, SharePoint or any synced folder - and Chrome or
Edge on the desktop.

  Publishing   You own this one. Ledger writes a snapshot of your visible
               containers into the shared folder a few seconds after every
               change, and again when you press Publish now.
  Viewing      Somebody else publishes. Ledger reads their snapshot and shows
               it read-only. Refresh pulls the latest, and it re-checks by
               itself once a minute.

WHAT VIEWERS SEE is set per container. Open a container's settings and set
"Visible to viewers" to Yes. Containers left at No are NOT WRITTEN TO THE
SHARED FILE AT ALL - they never leave your machine. In a folder other people
can open, absence is the only real way to hide something.

A viewer can read everything published, use the filters, read the reports and
print records. They cannot start timers, add or change anything, or restore a
backup.

Two things this is deliberately not:

  * Not access control. Anyone who can open the shared folder can read the
    published file directly, whatever Ledger shows them. Decide what to
    publish on that basis, and treat the folder's sharing list as the real
    boundary.
  * Not collaboration. Only the owner writes. Viewers cannot log their own
    time or tick their own attendance.

If you also use Ledger for your own work, viewing somebody else's is safe:
while viewing, Ledger never writes to your own stored data. Switch Sharing
back to Off and your own containers come back untouched.


FILTERS
-------
Every table - tasks, the cast, players, what's due and the report detail - has
a filter row under its headings. Columns with a fixed set of values give you a
dropdown listing only the values actually present, so no choice ever returns
nothing. Free-text columns filter as you type. Filters stack.

While anything is filtered a bar reads "Showing 8 of 16" with a Clear filters
button, so a filtered list can never be mistaken for missing data. Filters are
remembered between sessions - that bar is how you notice.


ROLEPLAY MODE
-------------
A container can be set to Roleplay when you create it, or later from its
settings. The machinery is identical - timers, planner, reports, printable
records, documents - but the vocabulary changes:

  Project    becomes  Campaign
  Task       becomes  Session
  Milestone  becomes  Plot arc
  Member     becomes  Player
  Person     becomes  Game Master
  Department becomes  System
  Due date   becomes  Session date

PLOT ARCS work like milestones, but a session can belong to SEVERAL arcs at
once. Click an arc's name to see every session linked to it and the total time
logged against that arc.

CAST is a per-campaign list of characters. A character belongs to a campaign,
not to a player, so the same person can play different characters in different
campaigns, and several characters in one campaign as they come and go. Each
has a name, an archetype (class, profession, or a short description), the
player behind it, and a state: Active, Retired or Deceased.

ATTENDANCE is recorded per session - tick who was at the table. Percentages
count only sessions marked Played, since those are the ones that happened; a
scheduled session is not a no-show. In the Players list, click any player to
see every character they have played and how many sessions they turned up to,
counted per campaign.

CAMPAIGN COST is an activity type for one-off spending such as a VTT licence
or a rulebook. Campaigns get the Cost field but not accounts - a table's
spending is one-off rather than a balance.

Switching a container between Work and Roleplay re-maps statuses and activity
types by position, and switching back restores them. Names, notes, dates, arc
links, cast and logged time are never touched.


SETTINGS
--------
The gear button in the header sets what the app assumes you are here for:
Work, Roleplay, or both. It decides what a fresh install starts with and what
a new container defaults to, plus the default currency for new containers.

It never hides or deletes anything you already have - a work container stays a
work container whatever the setting says.


SUPPORT
-------
Ledger is free and always will be. If it saves you a spreadsheet or earns a
place at your table, there is a tip jar at ko-fi.com/kraethas.


SHARING IT
----------
AphelionLedger.html is one self-contained file with no dependencies. E-mail
it, zip it, or put it on GitHub. The Aphelion mark is drawn as inline SVG
rather than loaded from anywhere, so the app never reaches out to the network
and works fully offline.

Whoever opens it gets an empty tracker of their own; your data stays in your
browser and is never inside the file itself.

MIT licensed - see LICENSE. Use it, fork it, modify it, ship it commercially.
No warranty.
