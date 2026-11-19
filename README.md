# sendworthy

Emails worth sending: energetic, humble, and impossible to ignore.

Sendworthy is a Claude Agent Skill that makes Claude write, reply to, and polish emails and professional messages in a warm, specific, forward-moving voice. It never sends anything on its own; it produces drafts for you to review.

## Before and after

**Flat**

> Hi Maya, I understand that volunteer spots are full. Thanks for letting me know. Regards, Sam

**Sendworthy**

> Hi Maya,
>
> Thank you so much for getting back to me, and congratulations on filling every volunteer spot for the spring summit. That says a lot about the community you have built!
>
> I'll complete the interest form this week, and I'd be glad to pitch in wherever it helps most at the next event.
>
> Best,
> Sam

## Features

- Energetic-and-humble tone rules: specifics and momentum instead of adjectives
- Shapes by email type: outreach, loop-closing, ongoing thread, request, follow-up, decline
- Length guidance (1-3 sentences for routine replies, 60-150 words for substantive ones)
- Greeting and sign-off table by recipient type
- Banned list: no em dashes, no "hope this email finds you well", and more
- Fact discipline: `[PLACEHOLDER]` for unknown facts, never claims actions you did not take
- Drafts only: never sends
- Self-check list before every draft
- Fully editable "Personalize me" block

## Install

### 1. Claude Code

macOS / Linux:

```bash
git clone https://github.com/Dexter3337/sendworthy.git
mkdir -p ~/.claude/skills && cp -r sendworthy/sendworthy ~/.claude/skills/sendworthy
```

Windows (PowerShell):

```powershell
git clone https://github.com/Dexter3337/sendworthy.git
New-Item -ItemType Directory -Force "$env:USERPROFILE\.claude\skills" | Out-Null
Copy-Item -Recurse sendworthy\sendworthy "$env:USERPROFILE\.claude\skills\sendworthy"
```

The skill ends up at `~/.claude/skills/sendworthy/` (macOS/Linux) or `%USERPROFILE%\.claude\skills\sendworthy\` (Windows).

### 2. Claude.ai / Claude desktop

1. Download `sendworthy.zip` from the latest GitHub Release.
2. Open Settings > Capabilities > Skills.
3. Upload the zip.

### 3. Claude API / Agent SDK

Point your skills configuration at the `sendworthy/` folder in this repo (it contains `SKILL.md`). See the Anthropic documentation for the current way to load skills in the API or Agent SDK.

## Personalize it

1. Open `sendworthy/SKILL.md`.
2. Find the "Personalize me" block at the top.
3. Replace each bracketed field ([YOUR NAME], [ONE-LINE BACKGROUND], [CURRENT ROLE OR PROGRAM], [GOAL], signatures) with your own details. Delete lines you do not need.
4. Optionally replace the example emails with ones in your own style.
5. Re-copy or re-zip the folder and reinstall.

## Usage examples

- "Reply to this email in my voice: [paste email]"
- "Draft a cold email to a hiring manager at [company] asking for a 15-minute chat."
- "Polish this message so it sounds warmer without getting longer."
- "Write a follow-up to my note from last week. They have not replied."
- "Decline this invitation politely."

## Tweak the tone

Edit the "The tone" section of `SKILL.md`. Want more formal? Remove the exclamation-mark allowance. Want warmer? Allow two interest lines. Add your own phrases to "Language" and your own pet peeves to "Banned".

## FAQ

**Does it send emails?** No. It drafts only.

**Will it invent facts?** It is told to use `[PLACEHOLDER]` for anything unknown and never to claim actions you have not taken.

**Why no em dashes?** They are a common marker of machine-written text. The skill uses periods, commas, colons or hyphens instead.

**Can I use it for non-email messages?** Yes, for most professional messages.

## Contributing

Issues and pull requests are welcome. Keep examples fictional and free of personal details.

## License

MIT. See [LICENSE](LICENSE).
