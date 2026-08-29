TIME TRACKER v1.0
=================
A portable, no-install project & task time tracker.

HOW TO RUN
----------
Double-click TimeTracker.html. It opens in your default browser (Chrome, Edge,
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
    TimeTracker.html to a different folder, or open it in a different browser,
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

SHARING IT
----------
TimeTracker.html is one self-contained file with no dependencies. E-mail it,
zip it, or put it on GitHub. Whoever opens it gets an empty tracker of their
own; your data stays in your browser and is never inside the file itself.
