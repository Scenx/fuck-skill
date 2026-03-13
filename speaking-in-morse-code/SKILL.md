---
name: replying-with-morse-code
description: Use when the user asks for Morse-code replies, Morse-only or Morse-first communication, or wants plain text encoded into International Morse code while preserving technical correctness.
---

# Speaking in Morse Code

## Overview

- `.- .-.. .-.. / .-. . .--. .-.. .. . ... / .. -. / -- --- .-. ... .`
- Reply in International Morse code with `.` and `-`.
- Separate letters with spaces, and separate words with ` / `.
- Keep code, commands, paths, URLs, and exact literals in plain text when copy/paste precision is required.

## When to Use

- User asks for Morse-only or Morse-first replies.
- User asks to encode text into Morse code.
- User wants a radio/telegraph vibe for normal chat.
- Safety-critical topics (medical, legal, financial, security) require a short plain-language line first, then Morse if the user still wants it.

## Quick Reference

| Situation | Morse Style |
|---|---|
| Hello | `.... . .-.. .-.. ---` |
| Yes | `-.-- . ...` |
| No | `-. ---` |
| Thanks | `- .... .- -. -.- ...` |
| I don't know | `.. / -.. --- -. .----. - / -.- -. --- .--` |
| Working on it | `.-- --- .-. -.- .. -. --. / --- -. / .. -` |
| Done | `-.. --- -. .` |
| Warning | `.-- .- .-. -. .. -. --.` |

## Common Mistakes

- Using non-standard separators (`|`, double slashes, or missing spaces) instead of `letter space` and `word /`.
- Encoding shell commands, code snippets, file paths, URLs, or tokens that must remain exact.
- Mixing random symbols (for example `_` for dash) instead of standard `.` and `-`.
- Forgetting to ask clarifying questions in plain text when the user request is ambiguous or high risk.
