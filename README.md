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
- Bulk import: paste questions or upload a Word, CSV or text file, check the list, then add. A ready-made Word template is downloadable from the question screen

**Students**
- Enter a personal code in the lab, read the instructions and start the timed exam
- Sign in to a profile with school code, admission number and PIN
- See subjects done and upcoming, exam records, and strengths and weaknesses by topic
- Practice sets with instant feedback, and a JAMB-style estimate out of 400

## Exam features

- Question grid during the exam, with flag for review
- Optional scientific calculator, switched on per subject
- Page-leave limit per exam (warns, counts, then submits automatically)
- Optional provisional score shown after submit, per exam
- Lesson notes: teachers paste or upload the note they taught from, and the system drafts the model answer and marking scheme for theory questions. The teacher checks and edits the draft
- AI marking check: a button in Account tests that the AI service is connected
- Administrators can extend time, issue 15-minute quick codes, rename or archive classes and subjects, and tick subjects and classes for each teacher

## Who can do what

- **Platform owner (creator):** the only person who can add a school. Adding a school gives it a school code straight away.
- **School administrator:** signs in with the email the owner registered, after setting a password from an invite email. Registers students and teachers, and sets exams.
- **Students:** enter the school code and their personal exam code in the lab, or school code, admission number and PIN for their profile.
- Nobody can register a school on their own. An account with no registered school can do nothing.

## How it is built

- One static page: `index.html`
- Supabase for the database, sign-in and server functions
- Access rules (row-level security) and server functions keep each school's data separate. Answer keys are only used on the server.
- The page contains the project's public key. That key is meant to be public; it does not give access to protected data.

## Run it

Host `index.html` on any static host. For GitHub Pages: Settings, then Pages, then deploy from the `main` branch, root folder.

## License

All rights reserved. See [LICENSE](LICENSE).
