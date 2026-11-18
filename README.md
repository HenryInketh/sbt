# SBT: School Based Test

A web portal for running school exams, practice sessions and performance analysis. Built for schools that test students on lab computers or phones, with teachers drafting questions remotely.

> Status: pilot version. Under testing with a first school.

## What it does

**School administrator**
- School profile, classes, subjects, students and teachers
- Personal, revocable links for each teacher
- Approves papers, schedules exams, opens and closes the exam lab
- Personal exam codes for each student, with a printable code sheet
- Live roll call, new codes, force submit
- Student PINs, result release, topic performance reports with criteria that only the administrator can change
- Per-subject switches for image, fill in the gap and theory questions

**Teachers**
- Draft questions through the term and submit to the administrator
- Objective (A to D), fill in the gap, theory, and image questions or image options
- Topic tags on every question

**Students**
- Enter a personal code in the lab, read the instructions and start the timed exam
- Sign in to a profile with school code, admission number and PIN
- See subjects done and upcoming, exam records, and strengths and weaknesses by topic
- Practice sets with instant feedback, and a JAMB-style estimate out of 400

## How it is built

- One static page: `index.html`
- Supabase for the database, sign-in and server functions
- Access rules (row-level security) and server functions keep each school's data separate. Answer keys are only used on the server.
- The page contains the project's public key. That key is meant to be public; it does not give access to protected data.

## Run it

Host `index.html` on any static host. For GitHub Pages: Settings, then Pages, then deploy from the `main` branch, root folder.

## License

All rights reserved. See [LICENSE](LICENSE).
