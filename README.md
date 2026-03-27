# OpenClaw Lead Gen + Outreach Pipeline

Multi-agent lead generation pipeline built with OpenClaw.
Researches targets, scores against ICP, drafts personalised emails,
and gates everything behind human approval before sending.

## Watch the live demo (~6 minutes)
https://www.loom.com/share/9177ae3501ea4baeb9f34af11dcdb689 

## What it does

**Agent 1 — Scout**
- Searches the web for 20 target companies in a given niche and location
- Scores each company against a 5-point ICP rubric (2 pts per criterion)
- Drops companies scoring below 7/10 automatically
- Stores qualified leads in memory for the next agent

**Agent 2 — Email Writer**
- Reads qualified leads from memory
- Visits each company website and finds one specific detail
- Drafts a 3-sentence personalised cold email per company
- Subject line under 45 characters, no buzzwords
- Stores all drafts in memory for approval

**Agent 3 — Approval Gate**
- Posts all email drafts to Discord
- Waits for: APPROVED, REJECT [numbers], or CANCEL
- Never sends without explicit human sign-off
- After approval: sends via Gmail and confirms

## Live run results
- Niche: B2B SaaS operations tools
- Location: London
- Raw candidates: 20
- Qualified leads: 18
- Emails drafted: 5 (personalised, research-backed, under 4 minutes)

## Skills included
- `icp-scorer` — ICP rubric and scoring logic
- `lead-scout` — 3-phase discovery and qualification
- `outreach-writer` — personalised email drafting rules
- `approval-sender` — approval gate and Gmail send logic

## Tech stack
OpenClaw · Claude Sonnet · DuckDuckGo web search · Discord · Custom SKILL.md

## How to use
1. Clone this repo
2. Copy skill folders into `~/.openclaw/skills/`
3. Add pipeline context to your `BOOTSTRAP.md`
4. Run: `openclaw tui`
5. Trigger: `Run the lead gen pipeline for [niche] companies in [location]`

## Available for projects
I build OpenClaw pipelines for agencies, B2B SaaS companies, and founders.

Upwork: https://www.upwork.com/freelancers/~01929f4fb2b803e9e4
Email: anas.awan@conciergeone.net
