---
title: Troubleshooting
description: What to do when Draftline will not open a book, will not update, or is doing something odd.
published: true
date: 2026-09-18T00:00:00.000Z
tags: reference, troubleshooting
editor: markdown
dateCreated: 2026-09-18T00:00:00.000Z
---

# Troubleshooting

## A book will not open, and says it is open somewhere else

It is. The same book cannot be open in two windows, and Draftline brings the
window that has it to the front instead of opening a second copy.

If no such window exists — the application was killed, or the machine lost
power — open the book again. Draftline notices the claim belongs to nothing
and takes it.

## "Draftline could not finish that"

Something failed in the background. The message says what. Your manuscript is
untouched: the notice appears instead of a screen that has quietly stopped
responding, which is what used to happen.

If it keeps appearing, close the book and reopen it. If it survives that,
**Report an Issue** in the menu, with what you were doing when it appeared.

## An update says it is available but will not download

Usually because the release is still being built. Publishing a release starts
its build, and for ten or fifteen minutes the packages do not exist yet. Wait
and try again.

If it persists, download the installer from the releases page by hand.

## Read Aloud will not start

It needs its voice model downloaded once, in **Settings → Read Aloud**. If the
download was interrupted, start it again from there.

## The cast is missing people, or has people who are not people

Draftline proposes a cast by reading the manuscript, and it is a guess.
Confirm the ones it got right, dismiss the rest, and add anyone it missed by
hand. Corrections stick.

Invented names are the hard case, which is unfortunate, since novels are full
of them.

## Something is slow

Large artwork is the usual answer. Print-ready wrap art is tens of megabytes,
and keeping a copy inside the book makes every save and every sync carry it.
**Book Details & Editions** can link the artwork instead — see
**[Book details and editions](/publishing/book-details-and-editions)**.

## I lost work

In order:

1. **Undo**, if you are still in the chapter. A hundred steps.
2. **[Chapter history](/writing/chapter-history)** for anything older.
3. Your own backup of the `.draftline` file.

Draftline saves a few seconds after you stop typing, and **Save & Quit** and
**Back to Library** both refuse to leave if the save fails — so work lost to
Draftline closing is not a thing that should happen. If it did, that is worth
reporting.

## Reporting something

**Help → Report an Issue** opens the tracker with the form started. Useful:
what you did, what happened, what you expected, your version (the start screen
shows it), and your platform.
