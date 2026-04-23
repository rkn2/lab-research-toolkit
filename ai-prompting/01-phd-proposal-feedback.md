# Example 1: Reviewing a PhD Proposal Draft

---

## Research context

A second-year PhD student has submitted a 15-page proposal draft before our meeting. The background section is solid, but the methodology is vague — it describes what they want to do without explaining how, and without justifying why their approach is appropriate for the problem. I need structured feedback I can share with them directly, not a general impression.

---

## The prompt

```
I am a professor in structural engineering. My PhD student has submitted a proposal draft.
I want you to act as a critical but constructive reviewer. Read the draft below and give
me structured feedback organized into three sections:

1. Strengths — what the student does well that should be preserved.
2. Critical gaps — the 2-3 most important problems that need to be fixed before this
   proposal is defensible. Be specific about what is missing or unclear, not just that
   something "needs more detail."
3. Specific language — 3 to 5 sentences or phrases from the draft that are vague or
   weak, with a suggested revision for each.

Focus especially on the methodology section. I want feedback that is honest and direct —
not encouraging for its own sake. This student is in their second year and needs to
understand what a dissertation committee will actually scrutinize.

[PASTE DRAFT HERE]
```

---

## Why I structured it this way

**Assigning a role explicitly.**
"Act as a critical but constructive reviewer" changes the tone of Claude's output. Without this, Claude defaults to a supportive register — it will find things to praise and frame problems gently. That is not useful when you need honest assessment. Naming the role shifts the default.

**Asking for three named sections.**
Structured output has two benefits: it forces Claude to organize its thinking rather than produce a stream of impressions, and it makes the output easier to share with the student. A wall of comments is hard to prioritize. Three labeled sections make it clear what matters most.

**Flagging the methodology explicitly.**
I already knew the methodology was the weak part. By naming it, I prevent Claude from spending equal time on things I am less concerned about. Claude does not know which section matters most to you — you have to tell it.

**"Honest and direct — not encouraging for its own sake."**
This is the most important phrase in the prompt. Claude is trained to be agreeable and tends toward diplomatic hedging. Naming this bias directly suppresses it. Without this instruction, you will get softened feedback that technically identifies problems but buries them in qualifications.

**"Second year" as context.**
Student level changes what feedback is appropriate. A first-year needs guidance on what a proposal is. A second-year needs to understand what a committee will scrutinize. Giving Claude this context produces feedback calibrated to the right standard.

---

## How to adapt this

**For a literature review draft:**
Replace "methodology section" with "literature synthesis" and change the three sections to: coverage (are key areas represented?), argument structure (does the review build toward a gap?), and citation quality (are claims properly supported?).

**For an abstract:**
Shorten the prompt significantly. Ask Claude to revise the abstract line by line rather than organize feedback into sections — the document is too short to need section structure.

**For a full dissertation chapter:**
Add a word limit for the feedback ("no more than 400 words per section") or Claude will generate very long output. For chapter-level review, also specify whether you want Claude to attend to argument structure, technical content, or writing clarity — it cannot do all three equally well at chapter scale.

**If the student is further along:**
Add: "This student is preparing to defend. Focus your criticism on the 1-2 problems a committee is most likely to push back on, not on lower-stakes issues." This narrows the feedback to what is actually high-stakes.
