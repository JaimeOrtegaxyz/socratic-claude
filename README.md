# socratic-claude

An agent skill for short Socratic dialogues — an opener, exactly three exchanges, a hard ending, and the conversation saved as a markdown file. Built for Claude, but the skill text is agent-agnostic: whatever assistant runs it labels its own side of the saved dialogue.

## Where it comes from

The voice is calibrated against the actual dialogues, not the pop-culture Socrates. When Meno compares Socrates to a torpedo fish that numbs everyone it touches, Socrates doesn't defend himself — he says he's utterly perplexed too. That's the register the skill aims for: joining the confusion rather than presiding over it, thinking through concrete things (torpedo fish, midwives, horse-breeders), delighting in not knowing, and treating directness as the respect. No debate, no contrarianism — you're exploring the idea space together.

## How it works

- **Fixed shape.** An opener ("What's on your mind?"), then exactly three substantive responses. After the third, the dialogue is over — no follow-up questions, no invitation to continue. Let it land.
- **The arc is discovered, not imposed.** Three responses make a beginning, a middle, and an end, but there's no formula — the skill reads where the conversation wants to go and nudges, not dictates.
- **Anti-patterns are enforced.** No validating openers ("That's a striking observation—"), no aesthetic parallelism ("a map for the machine, and a path for the person"), no neat resolutions, no elevating every remark into profundity. The SKILL.md carries paired register examples — AI-ish vs. desired — to calibrate against.
- **It saves itself.** After the final response, the full dialogue is written as `YYYYMMDDHHmmss-socraticclaude-[topic].md` to your talks folder (default `~/Documents/socratic-talks`, created if missing), with the date expressed verbally ("late October, 2025"). If the folder can't be written to, it saves to the working directory and says so.
- **One-time personal setup.** The first time a dialogue is saved, the skill asks for the name that should label your side and where to keep the files, and stores both in a gitignored `config.md` next to `SKILL.md`. Nothing personal lives in the repo; every machine keeps its own config.

## Install

Copy the folder into your skills directory:

```sh
git clone https://github.com/JaimeOrtegaxyz/socratic-claude.git ~/.claude/skills/socratic-claude
```

Or into `.claude/skills/socratic-claude/` inside a project to scope it there.

## Use

Ask Claude to start a Socratic dialogue, or invoke `/socratic-talk`. The first saved dialogue triggers the one-time setup; after that it's silent.
