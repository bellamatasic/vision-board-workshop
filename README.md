# vision-board-workshop

Landing and sign-up page for **The 2027 Vision Board Social**, a free virtual evening in December 2026.

## What's here

- `index.html`: the whole site in one static page (HTML, CSS and a small script). There's no build step.

## Sign-up form

The form asks for first name, email, how the person is making their board (`physical`, `digital` or `unsure`), and whether they want future emails.

Sign-ups aren't saved anywhere yet. To connect the form, set `SIGNUP_ENDPOINT` near the bottom of `index.html` to a Loops form endpoint:

```js
const SIGNUP_ENDPOINT = "https://app.loops.so/api/newsletter-form/YOUR_FORM_ID";
```

Each sign-up is sent with `userGroup=2027-vision-board-social`, `source=vision-board-interest-page`, `futureEmailsOptIn` and `boardType`. `boardType` is what lets reminders go to the right group.

## Preview locally

Open `index.html` in a browser, or run `python3 -m http.server` and go to http://localhost:8000.

## Deploy

It's a static site, so Vercel (or any static host) can serve the repository root as it is.
