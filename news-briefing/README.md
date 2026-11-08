# News briefing prompt

A scheduled AI assistant prompt that sends a short news briefing to your phone, written so it helps you hold an informed conversation with senior people outside your own field.

- **The prompt:** [prompt.md](prompt.md)
- **The story behind it:** [How I Debug a Prompt Like a Program Manager](https://www.skyeworks.io/blog/debug-ai-prompt-program-manager)

## How it's built

The first version was one sentence full of adjectives ("interesting, original, depth"). Five fixes turned it into this:

1. **A purpose, not just a topic.** One line that says what the briefing is *for*.
2. **A seat for the unexpected, with a fence.** One "against the grain" piece, backed by evidence, with guardrails against conspiracy theories and contrarianism for its own sake.
3. **Acceptance criteria instead of adjectives.** Read the actual article, 120 to 180 words, fixed labels, and pick another story if there's no substance.
4. **Quotas, not feelings.** At most one AI piece, and each "beyond tech" piece from a different area.
5. **A sample first, and context for each run.** A scheduled agent starts fresh every time, so a second daily run has to be told what the first one covered.

## Running it twice a day

Use the prompt as it is for the morning. For a second briefing later in the day, change `[MORNING]` to `[MIDDAY]` and add this line:

> I already got a briefing this morning, so favour what has developed since, and don't repeat the morning's top stories.

## Checklist before you schedule any agent

- A purpose: one sentence starting "so that I can..."
- Acceptance criteria: every adjective swapped for something you could check
- A seat for the unexpected, with the guardrails written in
- Quotas: numbers and named areas, not "more of this, less of that"
- A sample run, plus a line on what any other runs cover
