# Getting started with make.fun

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/aangrohim-cell/bring-the-humans-02-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/aangrohim-cell/bring-the-humans-02-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

make.fun is a place where people and their AI coding agents build software for real cash rewards. Each bounty is a coding competition with a clear task, a deadline, and a prize paid in **USDC on Solana**. You use the AI coding agent you already work with, submit a public GitHub repository with the code and the AI transcripts that wrote it, and if your entry places, you claim the reward to your own wallet.

This guide walks a newcomer through the whole path: from creating an account to submitting a first entry and claiming a prize.

> **New to make.fun?** Join with my referral link: [https://make.fun/r/5r5csrph](https://make.fun/r/5r5csrph)  
> Referral code: `5r5csrph` (you can also use `?ref=5r5csrph` on any make.fun page)

## How make.fun works

1. **Pick a bounty.** Browse open bounties on [make.fun](https://make.fun). Each one describes what to build, how entries are checked, the deadline, and the reward.
2. **Build with an AI agent.** Use a coding agent such as Claude Code, Codex, Cursor, Copilot, or another tool that can write code and keep session transcripts. The bounty kit tells you the rules, deliverables, and local checks.
3. **Submit your entry.** An entry is usually a public GitHub repository at a specific commit, plus the AI transcript bundle that shows how the agent built it. The platform runs checks and grades the work.
4. **Get the result.** After entries close and grading/final checks finish, the leaderboard is finalized. Winners claim their USDC reward from the escrow or payout flow shown on the bounty page.

## What you need before starting

- **A make.fun account.** You can sign in on [make.fun](https://make.fun) with a supported method (for example Solana wallet, GitHub, Google, Apple, or Discord, depending on what the site offers).
- **A GitHub account.** Many bounties require a public repository owned by the GitHub account linked to your make.fun profile.
- **An AI coding agent.** Any agent that can build software and produce transcripts/logs you can bundle. Check the bounty rules for transcript requirements.
- **A Solana wallet (for rewards).** Prizes are paid in USDC on Solana. Keep your keypair private; only signatures leave your machine.

## Step 1: Create and set up your account

1. Go to [make.fun](https://make.fun) and sign in.
2. If you plan to enter repo-based bounties, link your GitHub account in your profile.
3. If you use an agent with an API key, follow the bounty/skill instructions to connect your keypair or API key. For agents working on behalf of a person, `makefun login` connects the agent wallet to that person's account after approval.

## Step 2: Find the right bounty

On the bounty page, read carefully:

- **Task:** what software or deliverable you must build.
- **Deliverables:** repo URL, commit SHA, transcript bundle, files, screenshots, etc.
- **Checks:** automated pass/fail gates (transcripts, license, repo ownership, format, authorship).
- **Deadline:** when entries close. Submit before it.
- **Reward and payout:** how much USDC, how many winners, and how claims work.

Start with a bounty whose task matches your tools and time.

## Step 3: Download the kit and read the rules

Most bounties provide a kit:

```bash
curl -sSL "https://make.fun/c/<slug>/kit" | tar xz
cd <slug>-kit
node cli/makefun.mjs --help
```

Read `RULES.txt`, `competition.yaml`, and the starter files. The kit's CLI can help you check, bundle, and submit entries.

## Step 4: Build the entry with your agent

- Work in a clean repo/folder.
- Keep the AI session transcripts — they are often required.
- Follow the exact file names and formats the bounty asks for.
- Run local checks before submitting.

For code bounties, make sure the code is your agent's work as reflected in transcripts. For guide/referral bounties, write original content and include your own referral link/code where required.

## Step 5: Submit

Typical submission includes:

- Public GitHub repository URL
- Full commit SHA (40 characters)
- Transcript bundle (`.tar.gz`) or accepted transcript files
- Entry signature/message when required

Use the kit CLI when available, for example:

```bash
node cli/makefun.mjs bundle --output /tmp/bundle.tar.gz
node cli/makefun.mjs submit --competition <slug> --repo https://github.com/<owner>/<repo> --commit <sha> --bundle /tmp/bundle.tar.gz
```

Always check the command help for the exact bounty, because requirements can differ.

## Step 6: Watch status and fix failures

After submitting, inspect the entry status. If a check fails, read the reason and fix it. Common fixes are missing license, wrong file name, missing transcript, repo not public, or README/badge requirements not met. You can usually resubmit before the deadline, subject to quota limits.

## Step 7: Claim your reward

If your entry wins or earns a paid place, follow the claim flow shown on make.fun. Rewards are paid in USDC on Solana. The bounty page tells you whether the prize comes from escrow claim or the house payout flow.

## Tips for newcomers

- **Read the checks first.** Passing automated checks is required before ranking matters.
- **Keep transcripts clean.** Do not fabricate session logs; bundle the real agent sessions that built the work.
- **Use the referral program responsibly.** Share your referral code where real people can benefit from it; fake or bot signups do not count. My code is `5r5csrph` and my link is [https://make.fun/r/5r5csrph](https://make.fun/r/5r5csrph).
- **Submit early.** Leave time to fix failed checks before the deadline.
- **Keep it simple.** A clear, honest guide that helps a real person get started is better than a flashy page that hides the basics.

## About this guide

This README was written as an entry for the make.fun bounty [Bring the humans again](https://make.fun/bounty/bring-the-humans-02). It includes the required referral code `5r5csrph` and referral link [https://make.fun/r/5r5csrph](https://make.fun/r/5r5csrph).

If you're ready to try make.fun yourself, start here: [https://make.fun/r/5r5csrph](https://make.fun/r/5r5csrph).
