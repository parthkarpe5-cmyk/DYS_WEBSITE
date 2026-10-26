# Discover Yourself — Mind Upgrade

A mobile-friendly student workshop website for first- and third-semester students. Visitors take a three-question reflection quiz, receive an instant student-mode result and practical tip, explore four evening sessions, and try an embedded slot-booking form.

## Current status

**This is a front-end preview, not a live registration system.**

- Quiz scoring and personalised results work entirely in the browser.
- The booking form validates required fields and email format, then shows a demo confirmation.
- No answers or personal details are stored or sent to an organiser.
- Student rankings are not shown because no real participant dataset is connected.
- Dates, times, venue and syllabus are clearly marked sample content.
- Publishing this code does not imply college approval.

## Technology stack

| Component | Technology |
| --- | --- |
| Page structure | HTML5 |
| Styling | CSS3, responsive Grid and Flexbox |
| Interaction | Vanilla JavaScript |
| Fonts | DM Sans and Space Grotesk via Google Fonts |
| Backend / database | None |
| Build tooling / dependencies | None |

No framework, package installation, API key or environment file is required. Fonts use an external network request; system sans-serif fallbacks apply when unavailable.

## Run locally

### Open directly

Open `index.html` in any modern browser.

### Serve over HTTP

With Python 3 installed, run this command from the project directory:

```sh
python -m http.server 8000
```

Visit http://localhost:8000.

The copy-link button uses the Clipboard API. It normally works on localhost or HTTPS; browser permissions and direct-file access can restrict it.

## Project structure

```text
DYS_WEBSITE/
├── index.html       # Complete page, styles, quiz logic and demo form
├── README.md        # Setup, behaviour and launch requirements
└── .gitignore       # Local and generated files
```

The single-file structure makes the preview easy to share and deploy. There is no generated build directory.

## Visitor journey

1. Read a short introduction or start the three-tap quiz immediately.
2. Answer questions about attention, starting tasks and responding to setbacks.
3. Receive a student-mode result, reflection score and one practical action.
4. Explore four proposed evening sessions.
5. Complete the sample slot-booking form and see its demo confirmation.

## Quiz behaviour and limitations

Each question has three options, scored 2, 1 and 0 points in displayed order. Total scores range from 0 to 6.

- Scores of 5–6 show **The Steady Starter**.
- Lower scores select a pattern based on the lowest-scoring answer: **The Attention Explorer**, **The Last-Minute Sprinter**, or **The Thoughtful Replayer**.
- Ties currently use the first matching question.
- The quiz covers self-reported habits in the previous seven days.
- This is an informal reflection activity, not a validated personality test, psychological assessment or measure of intelligence or potential.
- Comparisons and percentiles must be calculated from actual participant responses before being displayed. Do not invent a participant count, ranking or testimonial.

## Proposed workshop content

| Evening | Theme | Example activity |
| --- | --- | --- |
| 1 | Focus and awareness | Breathing and attention observation |
| 2 | Emotions and choices | Practising a pause before responding |
| 3 | Effort and outcomes | Turning a worry into an actionable step |
| 4 | Values and consistency | Creating a seven-day habit experiment |

The workshop draws on the **Bhagavad Gita** as a source of philosophical reflection on everyday choices. That source is disclosed on the page. Students of all beliefs are welcome; prior knowledge is unnecessary, and guided meditation is described as optional.

Confirm the programme, activities, institutional requirements and event approval with organisers before launch.

## Customise

All content is in `index.html`:

- Edit the `questions` array in the script to change quiz questions and options.
- Edit `result()` to change result labels, scoring and practical tips.
- Update the four `.day` articles to change the session plan.
- Update `.details` and the booking slot dropdown together when finalising dates and times.
- Replace sample venue text and pending-confirmation notices only after details are confirmed.
- Adjust CSS variables in `:root` for colours.
- Keep philosophical-source information visible and accurate.

## Before collecting real registrations

The current form is deliberately a demo. To launch real booking:

1. Choose a data collection destination, such as a Google Form or a secured backend.
2. Replace the demo submit handler with that integration.
3. Tell students what information is collected, its purpose, who can access it and how to request deletion.
4. Validate submissions server-side where applicable, prevent duplicates and add abuse protection.
5. Confirm capacity and implement accurate availability; show success only after storage succeeds.
6. Add organiser contact information, final dates, timings, venue and any fee.
7. If adding comparisons, aggregate real quiz responses and disclose the comparison group, sample size and scoring method. Keep individual responses private.

Do not put private credentials in browser JavaScript.

## Deploy as a static website

This project works with static hosting, including GitHub Pages.

For GitHub Pages:

1. Push the files to the repository.
2. Open **Settings → Pages**.
3. Select **Deploy from a branch**.
4. Choose the `main` branch and `/ (root)` folder.
5. Save and wait for GitHub to provide the published URL.

No build command is needed. Deploying the static page does not activate bookings or create a database.

## Checks and review

JavaScript syntax was checked during preparation. Browser rendering and end-to-end behaviour were not verified in the restricted authoring environment.

Before sharing publicly, verify:

- Quiz completion, result text, retake and copy-link behaviour.
- Form required fields, invalid email handling and demo confirmation.
- Narrow phone layouts, keyboard navigation and readable text.
- All final event details and any live registration integration.

## License

No open-source license has been selected. Add a license if the repository owner wishes to grant reuse permissions.
