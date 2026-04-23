# Example 2: Structuring a Grant Narrative from Rough Notes

---

## Research context

I have a project concept and rough notes for an NSF proposal on using photogrammetry and machine learning to assess structural vulnerability in historic masonry buildings. The notes cover what I want to do, but they are not organized and some key pieces — significance, novelty, evaluation approach — are thin or missing. I need to turn this into a coherent 2-page Project Description before I can start writing.

---

## The prompt

```
I am writing an NSF proposal on using photogrammetry and machine learning to assess
structural vulnerability in historic masonry buildings. I have rough notes below. I need
help structuring a 2-page Project Description narrative.

Do not write the narrative yet. First, give me a proposed outline with section headers
and 1 to 2 sentences describing what each section should argue. Then identify any gaps
in my notes — places where I will need to add technical detail, cite prior work, or make
a clearer claim about significance or novelty.

My rough notes:
[PASTE NOTES]
```

---

## Why I structured it this way

**"Do not write the narrative yet."**
This is the most important phrase in the prompt. If you skip it, Claude writes the full narrative immediately. That output will be superficially coherent but shallow — it will fill in your gaps with generic statements rather than flagging them. An outline built on thin notes is easier to correct than prose built on thin notes, because the gaps are visible.

**Asking for gaps explicitly.**
Claude is good at noticing what is missing when you ask directly. Without this instruction it will produce output that glosses over missing pieces rather than naming them. You want to know where you need to do more work before you start writing, not discover it during revision.

**Keeping it to an outline stage.**
Grant writing is iterative. Getting structure right first, then developing each section separately, produces better results than asking Claude to do everything in one pass. Once you have an outline, you can go section by section: "Now write the significance section based on this outline and these notes."

**Naming the funder and document type.**
"NSF" and "Project Description" are meaningful constraints. NSF has specific expectations about intellectual merit, broader impacts, and how novelty is framed. Including these terms orients Claude to the right conventions without you having to explain them.

---

## How to adapt this

**For fellowship applications (NSF GRFP, etc.):**
Add: "This is a fellowship application, so the narrative should emphasize the student's intellectual development and trajectory, not just the project's technical contributions." Fellowships are evaluated on the person as much as the project — Claude needs this context to weight the sections correctly.

**For NEH or preservation-focused grants:**
Add: "The funder cares about cultural and humanities significance, not just technical innovation. Flag where my notes are thin on the argument for cultural impact." Technical framing that works for NSF can undermine an NEH application if the humanistic significance is not foregrounded.

**For multi-PI proposals:**
List the PIs and their roles at the top. Add: "Identify where the collaboration rationale is weak — the proposal needs to make clear why this work requires multiple investigators and what each contributes." NSF reviewers flag proposals where the collaboration feels incidental.

**When you are ready to write:**
Follow up with: "Now write the [section name] using the outline and filling in the gaps I've addressed." Go section by section. Asking Claude to write the whole narrative at once after the outline step is rarely better than section-by-section.
