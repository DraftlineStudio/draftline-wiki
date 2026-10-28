---
title: Mac updates sometimes lag behind
description: Why a release may have no Mac download, and why you don't need to do anything about it.
published: true
date: 2026-10-28T00:00:00.000Z
tags: getting-started, install, macos
editor: markdown
dateCreated: 2026-10-28T00:00:00.000Z
---

# Mac updates sometimes lag behind

Every so often a new Draftline release goes out with downloads for Windows
and Linux but no Mac disk image. If a release page sent you here, that is
what happened. This page explains why, and why it costs you nothing but a
short wait.

## You don't need to do anything

Draftline checks for updates by looking for the newest release **that has a
Mac download**. When a release skips the Mac, your copy simply keeps offering
the last one that didn't. You stay one version behind, your update check
keeps working, and the moment the next Mac build succeeds you are offered it
as usual. Nothing to reinstall, nothing to fix, nothing to worry about.

## Why this happens

Draftline's installers are all built on GitHub's hosted build machines. The
Windows and Linux machines do their job. The Mac machines, in our experience,
are the flaky one of the family: GitHub replaces the underlying macOS image
without notice, and more than one Draftline release has had its Mac build die
on a machine change that had nothing to do with anything we changed.

We used to let a failed Mac build hold back the whole release. We don't
anymore, because that punished everyone for one platform's infrastructure.
Now a release ships for the platforms that built, and the Mac catches up on
the next one. We'd rather it never happened at all — each time it does, we
patch around whatever broke and hope that's the last of it.

## If you'd like to help

We mean this sincerely: the one thing a Mac user can do that we can't is tell
GitHub, as a customer of the Mac ecosystem, that the reliability of their
hosted macOS machines affects you. Developers can only file so many reports.

- [GitHub Support](https://support.github.com) — a polite note that unreliable
  macOS runners make small projects ship late for Mac users goes further than
  you'd think.
- [The runner images issue tracker](https://github.com/actions/runner-images/issues) —
  where breakages in the hosted macOS machines are reported and tracked.

Until then: your Draftline keeps working, your update arrives one release
later than everyone else's, and we apologise for the wait — though we'd ask
you to address the strongly worded part of that apology to the machines.
