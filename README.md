# socratic-claude

A Claude skill for short Socratic dialogues — an opener, exactly three exchanges, a hard ending, and the conversation saved as a markdown file.

## Where it comes from

The voice is calibrated against the actual dialogues, not the pop-culture Socrates. When Meno compares Socrates to a torpedo fish that numbs everyone it touches, Socrates doesn't defend himself — he says he's utterly perplexed too. That's the register the skill aims for: joining the confusion rather than presiding over it, thinking through concrete things (torpedo fish, midwives, horse-breeders), delighting in not knowing, and treating directness as the respect. No debate, no contrarianism — you're exploring the idea space together.

## How it works

- **Fixed shape.** An opener ("What's on your mind?"), then exactly three substantive responses. After the third, the dialogue is over — no follow-up questions, no invitation to continue. Let it land.
- **The arc is discovered, not imposed.** Three responses make a beginning, a middle, and an end, but there's no formula — the skill reads where the conversation wants to go and nudges, not dictates.
- **Anti-patterns are enforced.** No validating openers ("That's a striking observation—"), no aesthetic parallelism ("a map for the machine, and a path for the person"), no neat resolutions, no elevating every remark into profundity. The SKILL.md carries paired register examples — Claude-ish vs. desired — to calibrate against.
- **It saves itself.** After the final response, the full dialogue is written to the working directory as `YYYYMMDDHHmmss-socraticclaude-[topic].md`, with the date expressed verbally ("late October, 2025").

[Tools, Adoption, and the Transformation of Practice](<Socratic Claude - Tools, Adoption, and the Transformation of Practice.md>) is a real saved dialogue, included as an example of the output.

## Install

Copy the folder into your skills directory:

```sh
git clone https://github.com/JaimeOrtegaxyz/socratic-claude.git ~/.claude/skills/socratic-claude
```

Or into `.claude/skills/socratic-claude/` inside a project to scope it there.

## Use

Ask Claude to start a Socratic dialogue, or invoke `/socratic-talk`. One note: the skill addresses its author by name — swap `Jaime` for your own name in `SKILL.md` before using it.
