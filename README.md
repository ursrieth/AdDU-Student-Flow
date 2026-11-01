# AdDU Student Flow

An academic command center for students. Open it and see what you need to work on today within five seconds.

> Unofficial student project. Not affiliated with or endorsed by Ateneo de Davao University.

Day 1 of a 7-day, 7-product challenge. The goal is to learn whether a real problem is solved, not to ship the most code.

## The problem

Students forget deadlines, exams, and requirements because the information is scattered across group chats, LMS pages, notebooks, and memory.

## What it does

- **Today:** a count of what to work on today, one "Start here" card for the top item, then the rest of the list.
- **Automatic prioritizing:** overdue items first, then by how close the deadline is and what type it is (exams outweigh quizzes, quizzes outweigh assignments).
- **Start-early reminders:** each deadline has a head start (for example 5 days for an exam). It appears in Today from that day.
- **Subjects:** one card per class with progress, overdue count, and the next exam countdown.
- **Calendar:** month view with a dot per deadline and a day panel for details and reminders.
- **Quick edit:** tap a deadline to change it, tick the box to finish it, undo within five seconds.

## Run it

No build step and no dependencies.

```bash
git clone https://github.com/ursrieth/addu-student-flow.git
cd addu-student-flow
# open index.html in a browser, or serve it:
python3 -m http.server 8000
```

In VS Code, the Live Server extension works too. Fonts load from Google Fonts, so the first open needs a connection.

## Where your data lives

Everything is saved in the browser's `localStorage` under the key `addu-student-flow.v1`. It stays on that device and browser. Clearing site data erases it, and a phone and a laptop do not sync.

The first load shows example classes. Use "Clear examples" to start with your own.

## Day 1 success test

Get three students to use it for a day.

1. Hand it over cold. Ask "What is due today?" Pass if they answer within five seconds without scrolling.
2. Have them add their real next three deadlines.
3. The next morning, check whether they opened it again without being asked.

If they do not come back, diagnose the product first. Is the first screen answering the right question? Is adding a deadline too slow?

## Known limits

- No phone notifications. Reminders only show inside the app.
- No sync between devices and no accounts.
- Dates use the device's local time.

## Ideas to test only if students ask for them

- Install to the home screen so it opens like an app.
- Import deadlines from a syllabus or class schedule.
- Share a subject's deadlines with classmates.

## Structure

```
index.html   the whole app: markup, styles, and script
```
