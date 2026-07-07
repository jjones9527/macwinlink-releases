# Contributing to MacWinlink

Thanks for your interest in helping MacWinlink improve.

## This is a distribution-only repository

**No source code lives in this repo.**  This repo (`jjones9527/macwinlink-releases`) exists solely to:

- Distribute public beta builds via [Releases](../../releases)
- Collect bug reports and feature requests via [Issues](../../issues)

**Pull requests will not be accepted here.**  There is nothing here to change with code — no source, no test suite, no CI.  Any PR opened against this repo will be closed with a pointer to this page.

## What you *can* contribute

### File a bug report

Open a new [issue](../../issues/new/choose) and choose **Bug report**.  Include your macOS version, MacWinlink beta version, and clear steps to reproduce.  Screenshots and log excerpts help enormously.

### Request a feature

Open a new [issue](../../issues/new/choose) and choose **Feature request**.  Describe the problem you're trying to solve, not just the solution you have in mind — this makes it easier to evaluate against similar requests.

### Test beta builds

Every download and honest report is useful.  If you use MacWinlink over the air on a mode or radio configuration nobody else has tried, your session logs are gold.

## Where the source code lives

MacWinlink's source, contributor guidelines, code discussions, and full development history are at **[ARSFI/MacWinlink](https://github.com/ARSFI/MacWinlink)**.

Code-level contributions (pull requests, protocol proposals, transport implementations, test fixtures, etc.) should go there — not here.  If you're a developer looking to contribute code, start with the ARSFI/MacWinlink `CONTRIBUTING.md` and `docs/` directory.

## How this repo's feedback flows upstream

1. You file an issue here.
2. The maintainer triages, reviews, may ask for more info.
3. Confirmed issues get opened in the ARSFI/MacWinlink repo, where the code lives.
4. Fixes and features ship in a subsequent public beta released here.
5. You'll be notified in the original issue when your report has been actioned.

This funnel exists because keeping public beta feedback in one focused place makes triage tractable — the ARSFI repo is where active development happens, and mixing beta-tester issues into the developer issue queue would drown both.

Thanks for testing.
