# Review instructions

This repository is a public GitHub Pages site: the homepage and privacy policy of a private Google
OAuth app, served from `main` with no build step. `README.md` says what each file is. Everything
merged here is public on the open web within minutes.

## What Important means here

Reserve 🔴 Important for a change that would publish the wrong thing or break the app's
verification, because an Important inline comment fails the required `claude review` check and
holds the merge:

- a secret, token, client secret or personal data in the diff;
- a page whose app name no longer matches the name on the OAuth consent screen, as `README.md`
  requires of `index.html`;
- a change that moves or removes the privacy policy at `/privacy`, or the homepage's link to it;
- a privacy policy that states a use of Google user data the app does not make, or omits one it
  does;
- a script, form or third-party resource added to a page.

Wording, style, ordering and naming are 🟡 Nit at most.

## Nit volume

Report at most five nits and give the rest as a count in the summary. After the first review of a
pull request, report Important findings only.

## Skip

Post no findings on what the `pre-commit (whole tree)` check already enforces: gitleaks.

## Verification bar

A claim about what a file or instruction does cites the `file:line` it rests on, not an inference
from a name.

## Summary shape

Open the summary with a one-line tally, such as `1 important, 3 nits`, or `No important findings`.
