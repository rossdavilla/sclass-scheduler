# Semester Grid — Class Schedule Generator

A single-file web app for building weekly class-schedule tables to paste into Google Docs.

**Live:** https://rossdavilla.github.io/sclass-scheduler/

## What it does
- Pick a class, set the term dates and class days — the weekly grid builds itself (one row per week).
- Load a past semester, drag lectures / exams / reviews onto the calendar, mark no-class days.
- **Copy table** (8″) straight into a Google Doc, or download `.doc` / `.html`.
- **Save & load** whole schedules — copy/paste a code into your Google Sheet, or use **Direct sync**
  to read/write them automatically via a bound Google Apps Script Web App (paste your `…/exec` URL
  into the Direct sync box once; it's remembered in your browser).

Everything runs client-side — the whole app is the single `index.html`.
