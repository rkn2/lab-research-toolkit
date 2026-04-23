# Example 3: Extracting Themes and Gaps from a Paper Collection

---

## Research context

I have accumulated 25 papers on image-based crack detection in historic masonry. I want to identify what the field has not addressed — specifically gaps in 3D analysis and structural context — before writing the research gap paragraph in a paper introduction. Reading and synthesizing 25 abstracts by hand is slow. I want Claude to do the first pass so I can focus on evaluating whether the gaps it finds are real.

---

## The prompt

```
I am reviewing literature on image-based crack detection in historic masonry. Below are
the titles and abstracts of papers I have collected. Your task is to identify patterns
and gaps across this collection.

First, group the papers into 3 to 5 thematic clusters based on their methods or focus.
Give each cluster a short label and one sentence explaining what the papers in it share.

Then identify 2 to 3 gaps — things that appear to be consistently absent across the
collection. Be specific: a gap is not "more work is needed" but a methodological choice,
a scale of analysis, a data type, or a type of structure that no paper addresses.

Do not summarize each paper individually. Work at the level of the whole collection.

Abstracts:
[PASTE ABSTRACTS]
```

---

## Why I structured it this way

**"Do not summarize each paper individually."**
Without this instruction, Claude produces a numbered list of 25 summaries. That is not useful — you already have the abstracts. The instruction forces Claude to work at the level of the collection, which is the actual task.

**Defining what a gap is.**
"A gap is not 'more work is needed' but a methodological choice, a scale of analysis..." This matters. If you do not define it, Claude produces vague gap statements like "future research should explore larger datasets." That is not a citable gap. A gap should be specific enough that you could write a research question around it.

**Clustering before gap-finding.**
Asking for clusters first structures Claude's analysis. It has to categorize before it can compare, which leads to more specific gap identification. Skipping the clustering step and asking directly for gaps often produces shallower results.

**Using abstracts, not full papers.**
Abstracts are sufficient for thematic clustering and gap analysis. Pasting full papers would make the prompt extremely long and does not improve the output for this task. If you want Claude to check specific methodological details, you can follow up by pasting individual sections from the papers that matter most.

**Limiting to 2 to 3 gaps.**
Without a number, Claude may list 6 or 7 gaps of uneven quality. A short list forces prioritization and makes the output more useful for writing. You can always ask for more if needed.

---

## How to adapt this

**For a systematic review:**
Add: "Also flag any methodological domains that appear in fewer than 3 papers — these may represent underexplored areas worth justifying in a review protocol." This is useful when you need to document coverage formally.

**For cross-disciplinary collections:**
If your papers come from different fields (structural engineering, computer vision, heritage conservation), add this at the top: "These papers come from multiple disciplines. When clustering, keep disciplinary differences visible rather than collapsing them." Otherwise Claude will merge clusters that should stay separate.

**For student use:**
This is a useful exercise to assign: give students the same set of abstracts and ask them to do their own clustering and gap identification before running the prompt. Comparing their analysis to Claude's output reveals where their reading was selective or where they missed patterns — which is a good basis for discussion.

**When you want to go deeper on one cluster:**
After the initial output, follow up with: "For the cluster on [label], paste the abstracts again and identify the 2 most-cited methodological limitations mentioned across those papers." This drills into a specific area without rerunning the full prompt.
