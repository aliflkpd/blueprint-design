# Blueprint Design

A Claude Code skill for designing a product or feature from zero: generate hypotheses, converge them into concrete prototypes, and validate which ones the business actually needs. It encodes a step-by-step method for going from a raw brief to a deliverable ready for real stakeholders, developed by working through a real multi-asset trading platform case study end to end, but the method itself is general-purpose product design, not a test-taking trick. Use it for a graded case study or take-home assignment, a 0-to-1 feature, or a real discovery effort with a business team, they all run on the same underlying process.

A blueprint isn't the building, it's what makes the building sound enough to actually construct. This skill covers the reasoning and documentation phases that generate and narrow down hypotheses before committing real effort to one, but it's built to feed directly into the real hi-fi design work that follows, not to stop at a well-organized FigJam board.

The core idea: **good product design is judged on the visible thinking, not just the final screens, whether the judge is a stakeholder deciding what to fund or a grader scoring an assignment.** This skill pushes Claude to produce evidence of that thinking at every step, documented assumptions, traceable HMW statements, real UI references instead of guesses, and a coverage check that catches gaps before they become a deduction or a stakeholder objection.

## What it does

When triggered, Claude will work through a design brief in phases instead of jumping straight to screens:

1. Explain the brief in the user's terms, without assuming domain fluency
2. Lock explicit assumptions before designing (with research backing numbers, not guesses)
3. Confirm hard constraints (platform, format, language) explicitly rather than inferring them
4. Frame the problem, then generate How Might We (HMW) statements
5. Build personas grounded in the brief, then validate every HMW against every pain point to catch gaps
6. Prioritize (P0-P3) so a limited slide/page budget goes to what matters most
7. Converge HMWs into concrete Solution Concepts before touching flow
8. Ground interaction/pattern decisions in real references (Mobbin, Lazyweb, WebSearch), not memory
9. Curate success metrics to a few primary ones instead of an unfocused list
10. Only then design the user flow
11. Build the hi-fi screens, then audit whether the terminology and units actually read like the real domain instead of a retail default
12. Produce the final deliverable (a stakeholder deck or a case-study submission), cohesive with the product's own design language and traceable back to every requirement or validated decision

It also describes how to keep a living markdown decision document and a parallel FigJam board in sync throughout, and how to handle reopening a decision when new information (or a stakeholder) invalidates something already "resolved."

## Install

Copy the folder into your personal skills directory:

```bash
cp -r blueprint-design ~/.claude/skills/
```

Or clone this repo directly into `~/.claude/skills/` if it's the only thing in it.

Claude Code picks up skills automatically from that directory. No restart or configuration needed.

## Usage

You don't need to invoke this by name. It's designed to trigger automatically when you:
- Are designing a product or feature from zero and want to generate hypotheses before committing to one
- Share a case study document or take-home design brief (a compressed instance of the same process)
- Ask to work through personas, HMW statements, problem framing, or prioritization for a design exercise
- Want a living decision log alongside a FigJam board while designing
- Are deciding on a UI interaction pattern and should check real references first
- Need to prep decisions or prototypes for a real discussion and validation with business stakeholders

You can also invoke it explicitly if you use it as a slash command or reference it by name, depending on your Claude Code setup.

## Notes

- This skill assumes access to FigJam (via the Figma MCP plugin) and web/visual research tools (WebSearch, and optionally Mobbin/Lazyweb MCP plugins) for the reference-gathering phases. Without those, the reasoning phases (assumptions, HMW, prioritization, gap analysis) still work fine, Claude will just skip the parts that need a specific tool it doesn't have.
- Written from one real case study, but the phases are domain-agnostic and apply equally to real 0-to-1 product work. It has not yet been tested across a wide variety of case study types or real business briefs (contribution and feedback welcome).

## License

MIT, see `LICENSE`.
