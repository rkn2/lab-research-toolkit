# Example 6: Stress-Testing a Research Argument Before Writing It Up

---

## Research context

I have a core claim that I want to make in a paper: that 3D geometric features derived from photogrammetric models outperform 2D visual inspection for predicting structural vulnerability in historic masonry. I believe it, my results support it, but I know reviewers will push back. I want to find the weakest points in the argument before I commit them to prose — not after two rounds of review.

---

## The prompt

```
I am going to give you a research argument. Your job is to attack it.

The argument: Geometric features extracted from photogrammetric 3D models of historic
masonry walls — specifically surface deformation, out-of-plane displacement, and crack
topology — can predict structural vulnerability more accurately than 2D visual inspection
alone. This holds even for buildings where photogrammetric resolution is limited by site
access constraints.

Find the 3 weakest points in this argument. For each one:
- State the weakness precisely. Do not just say "this is unclear" — explain what
  assumption is being made and why that assumption might fail.
- Describe what kind of evidence or experiment would expose this weakness.
- If you think the weakness is fatal to the argument as stated, say so.

Do not soften this. I need to know what a skeptical reviewer would say, not what a
supportive colleague would say.
```

---

## Why I structured it this way

**"Your job is to attack it."**
This is the most important reframe in the prompt. Claude's default is to engage charitably with an argument — to find what is right about it. This instruction reverses that default. Without it, Claude will identify weaknesses but frame them diplomatically, which makes them easier to dismiss. Framing it as an attack produces sharper, more useful criticism.

**State the argument as precisely as possible.**
The quality of the attack depends entirely on the quality of the target. A vague argument ("3D is better than 2D for assessing masonry") produces vague criticism. A precise argument — naming the specific features, the specific comparison, and the specific condition (resolution limits from site access) — gives Claude something to actually stress-test. Writing the argument out precisely is valuable in itself: if you cannot state it in 3 to 4 sentences, it is not ready to be written up.

**Asking for the evidence that would expose each weakness.**
This is what makes the feedback actionable. "This is a weak assumption" tells you there is a problem but not what to do about it. "Here is the experiment that would falsify this claim" tells you either what to run before submission or what to acknowledge explicitly as a limitation. The difference matters.

**"If you think the weakness is fatal, say so."**
Without this, Claude hedges. Every weakness becomes "a potential concern that could be addressed with further work." You need to know whether there is a foundational problem — one that requires reconceptualizing the argument — versus a surface problem that you can handle in the discussion section. Asking Claude to make this judgment explicitly forces a clearer response.

**"Not what a supportive colleague would say."**
Reviewers are not supportive colleagues. The framing of the prompt should match the framing of the actual test your argument will face. This phrase calibrates Claude's register to match what peer review actually feels like.

---

## How to adapt this

**Before submitting a paper:**
Run the abstract's central argument through this prompt. If Claude identifies a fatal flaw, better to know before reviewers do. If it finds only manageable weaknesses, the output tells you what to address in the discussion section.

**For dissertation defense preparation:**
Have the student state their dissertation's central argument in 3 to 4 sentences, then run this prompt together. Use the output to prepare answers for likely committee questions. Students who have thought through the strongest counterarguments to their own work defend much more confidently than those who have not.

**For reviewing a collaborator's draft:**
Frame it as: "Here is the central argument as I understand it from this draft." Run the attack, then check whether the manuscript adequately defends against each weakness. This is a faster way to identify whether a draft needs structural revision versus line editing.

**For weaker arguments:**
If the argument is still early-stage, change the last instruction to: "For each weakness, also suggest how the argument could be restated to avoid it." This turns the attack into a tool for refining the argument rather than just auditing it.

**Running this yourself first:**
Before giving this prompt to Claude, try writing the 3 weaknesses yourself. Then compare. If Claude finds weaknesses you did not think of, those are the ones most likely to appear in review. If you thought of the same ones Claude did, the argument is probably in good shape.
