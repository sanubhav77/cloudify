# Cloudify GitHub Repo — Pre-Application Verification Checklist

This needs to be done BEFORE submitting the Sierra and Lindy applications. Both companies will look at the GitHub link, and Cloudify is the single biggest lever in your CV/cover letter for both.

**Time budget**: 30-45 minutes for a clean polish; 10 minutes for the bare minimum.

---

## Bare minimum (10 min) — non-negotiable before applying

- [ ] **Repo is public** — go to GitHub repo settings → confirm visibility is "public", not "private"
- [ ] **Default branch is `main`** (not a half-finished feature branch)
- [ ] **README.md exists at root** and renders properly
- [ ] **README opens with what Cloudify does in 2 lines**, not generic "TartanHacks 2026 project"
- [ ] **No leaked secrets**: `git log` for any committed `.env`, API keys, or `.pem` files. If found, rotate the keys immediately + scrub via [git-filter-repo](https://github.com/newren/git-filter-repo)
- [ ] **No personal info**: scrub any teammates' personal email/phone numbers from commit history if applicable
- [ ] **License file** (MIT recommended for hackathon code) — shows you understand OSS norms

## Recommended polish (additional 30 min)

- [ ] **README has a 1-line tagline**: "Multi-agent automation that takes full-stack cloud migration from days to under 20 minutes via OpenAI + Anthropic Claude APIs and Dedalus SDK."
- [ ] **README has a "Why" section** (1 paragraph) — what problem this solves, why agents not scripts
- [ ] **README has a quickstart**: `git clone ... && npm install && npm run cloudify --target=AWS` (or whatever the actual run command is)
- [ ] **Architecture diagram** — even a hand-drawn whiteboard photo or a Mermaid diagram in the README is enough. Recruiters skim for diagrams.
- [ ] **Demo gif or video** in README. If there's a working demo, record a 30-second screen capture with [Kap](https://getkap.co/) or QuickTime.
- [ ] **Pin the repo on your GitHub profile** — both Sierra and Lindy will check your profile, not just the repo
- [ ] **At least 2-3 meaningful commits in your name** — if your team co-built, make sure your contributions are visible in `git log` (use `git shortlog -s` to verify)
- [ ] **List of supported stacks** in README (the "8+ stack configurations" claim — name them)
- [ ] **Acknowledge teammates** in README if hackathon was team-built — it shows integrity
- [ ] **Tag a release** (`v0.1.0` or similar) — signals shipping intent

## What to AVOID

- ❌ **Do not** delete teammates' commits to inflate your contribution stats — visible to anyone running `git log`
- ❌ **Do not** post fake stars / fake forks — both companies have engineers who will spot it
- ❌ **Do not** write a flowery README full of "revolutionizing" / "next-generation" / "leveraged" — direct technical language only
- ❌ **Do not** include placeholder TODOs in the README ("// TODO: add docs") — looks unfinished

## Pin the repo to your profile

GitHub profile → "Customize your pins" → select Cloudify. Sierra and Lindy will land on your profile from your application; the pinned repo is what they see first.

## What good looks like (1-page README structure)

```markdown
# Cloudify — Agentic Cloud Migration

Multi-agent automation that takes full-stack cloud migration from days to
under 20 minutes. Built at TartanHacks 2026.

## Why

Migrating a production app between AWS / GCP / Heroku usually takes days
of human work — IaC rewrites, dependency mapping, secret rotation, smoke
tests. Cloudify decomposes the work into agent-callable skills and runs
them with deterministic guardrails.

## How it works

[architecture diagram or mermaid graph]

- Agent orchestration via Dedalus SDK
- OpenAI + Anthropic Claude as backing models
- Skill registry: dependency analysis, IaC generation, secret rotation,
  smoke-test validation
- Deterministic guardrails on each agent decision

## Supported stacks

- Node + PostgreSQL → AWS / GCP / Heroku
- Python + Django + Postgres → ...
- [list 8+ here]

## Quickstart

git clone https://github.com/<you>/cloudify
cd cloudify
npm install
export OPENAI_API_KEY=...
export ANTHROPIC_API_KEY=...
npm run cloudify --source=heroku --target=aws

## Demo

[gif here]

## Built at TartanHacks 2026

By [your name] + [teammates]. Awarded [if applicable].

## License

MIT
```

## After polish: tell me when done

Once the repo is clean and pinned, we can kick off the actual applications:
- Sierra (with Block H answers from `reports/001-sierra-application-answers.md` + PDF from `output/cv-anmol-sahu-sierra-2026-04-25.pdf`)
- Lindy (with Block H answers from `reports/003-lindy-application-answers.md` + PDF from `output/cv-anmol-sahu-lindy-2026-04-25.pdf`)
- Cohere (with cover letter explicitly requesting SF/NY office, PDF from `output/cv-anmol-sahu-cohere-2026-04-25.pdf`)
