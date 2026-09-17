# Contributing to a bitbaum repository

Anyone can join or fork this work. What this file settles is what happens to
a contribution once it lands, so that the option to change the licence later
stays with the project and the credit for a change stays with its author.

This file lives in `bitbaum/.github` and applies to every repository in the
organisation that does not carry its own.

## What your sign-off means

Every commit in an outside pull request must carry a sign-off line:

    Signed-off-by: Your Name <you@example.org>

`git commit -s` adds it. By adding it you certify two things.

**1. The Developer Certificate of Origin, version 1.1.** In short: you wrote
the change, or have the right to submit it under this project's licence, and
you understand the contribution and your sign-off are public and permanent.
Full text: <https://developercertificate.org/>.

**2. A licence grant to the project.** You grant Cato, the maintainer, a
perpetual, worldwide, royalty-free, irrevocable licence to use, reproduce,
modify, distribute and sublicense your contribution, and to release it under
any licence the project adopts in future. You keep your copyright and every
right to use your own work elsewhere. This grant is what makes it possible to
relicense without tracking down every past contributor for consent.

## How an outside pull request merges

An automated sweep (`bitbaum/fleet`, `scripts/ci/auto-merge-sweep.sh`) merges
a pull request from outside the organisation once two things are true:

1. **every commit is signed off**, and
2. **a maintainer has approved the pull request's latest commit.**

Until both hold, the sweep leaves the pull request open and says which is
missing. The two are separate on purpose: the sign-off settles licensing, and
the review settles whether the code is safe to run — every repository here
deploys on merge. An approval covers the commit it was given on; pushing a new
commit needs a new approval.

Members commit under the maintainer's own identity and are not asked to
certify to themselves.

## Credit, and what it is worth today

Your name stays on your commits, and the organisation's nightly origin proofs
timestamp them.

A governed rule in Solon — `originator_share`, version 1 — sends a tenth of a
product's net revenue to the originators of the code it uses. Today an
originator means a repository's first author, there is no revenue yet, and a
contribution to an existing repository earns no share. Changing that is a
Solon vote, not a promise this file can make.

## Origin

Git dates are set by whoever commits, so they prove nothing about who was
first. The organisation stamps every repository's HEAD nightly through
OpenTimestamps and asks Software Heritage to archive it, and publishes the
proofs in `bitbaum/fleet` under `proofs/origin/` and the readable register at
<https://github.com/bitbaum/fleet/blob/main/registers/origin.json>. Your
signed-off commit becomes part of that record the night it lands.

## The usual

Run the repository's `verify` script before opening a PR. Keep a PR to one
change. Write the commit message for the person reading `git log` in a year.
