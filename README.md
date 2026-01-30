# ChatGPT Context Hygiene

This repository collects practical notes and patterns around long-context usage with ChatGPT and other LLMs.

It focuses on:
- early signals of context degradation
- drift vs. hard failure
- repetition, constraint erosion, and implicit state overload
- when recovery is still possible vs. when restarting is cheaper
- simple “context hygiene” practices for long-running sessions

This is **not** about prompt tricks or model limits.
It’s about recognizing when a conversation stops behaving deterministically and starts carrying too much hidden state.

## Observed degradation signals

Common early indicators:
- repetition of already-settled decisions
- polite but empty restatements
- gradual constraint drift
- increased hedging or re-explaining
- loss of prioritization clarity

These usually appear **before** any hard context limit is reached.

## Practical heuristics

Some patterns that proved reliable in practice:
- Treat long chats as having a “half-life”
- If a context dump can’t fit in ~10 lines, the split is already late
- Restarting early is cheaper than recovering late
- Visible signals beat gut feeling

## Scope

This repo intentionally stays lightweight:
- no code
- no tools
- no monetization
- no prescriptions

Just shared observations from real usage.

Contributions and discussion are welcome.

