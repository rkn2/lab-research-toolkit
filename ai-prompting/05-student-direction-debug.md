# Example 5: Diagnosing When a Student's Direction Is Unclear

---

## Research context

A third-year PhD student is technically capable — their code works, their scans are clean, their models converge. But in our last three meetings their research question has shifted in a different direction each time, and I am not sure whether the problem is scope, framing, confidence, or something about the project itself that is genuinely unresolved. I want to think through this before our next meeting rather than go in with the wrong diagnosis.

---

## The prompt

```
I am a PhD advisor. I have a student whose research direction has become unclear. I want
to think through what might be going on before our next meeting.

Here is what the student is working on, as I understand it:
The student is using photogrammetric point clouds of historic masonry walls to detect
crack patterns. The original goal was to build a damage classification model. Over the
past few months they have shifted toward also wanting to do structural assessment, then
toward wanting to compare photogrammetry and LiDAR as acquisition methods, and most
recently toward writing a methods paper rather than an application paper.

Here is what I have observed in recent meetings:
They come in with new ideas rather than progress on the previous direction. They do not
push back when I suggest constraints — they agree and then come back with something
different. They seem more comfortable in the literature than in their own results.

My current hypothesis:
I think they are avoiding the hard part of the project — generating ground truth labels
for the damage classification — because that work is slow and unglamorous, and they are
filling the time with scope expansion instead.

Play devil's advocate against my hypothesis. Give me 3 alternative explanations for what
I am observing that are plausible given what I have told you. They do not need to be
fully convincing, but they should be different in kind from my hypothesis.

Then suggest 2 to 3 questions I could ask in our next meeting that would help me
distinguish between my hypothesis and the alternatives.
```

---

## Why I structured it this way

**Stating my hypothesis first.**
This is counterintuitive. You might think giving your hypothesis biases the output. In practice, the opposite is true: if you do not give Claude your working theory, it will mirror your framing back to you in different words, which is not useful. By naming your hypothesis and explicitly asking Claude to push back on it, you get alternatives rather than validation.

**"Play devil's advocate."**
This is a reliable instruction for generating counterarguments. Claude's default is to be agreeable — it will find reasons your hypothesis is correct unless you explicitly ask it not to. This phrase reliably breaks that pattern.

**Describing behavior, not character.**
Notice that the observations are behavioral ("they come in with new ideas rather than progress") rather than character judgments ("they are unfocused" or "they lack discipline"). Behavioral descriptions give Claude something concrete to reason about. Character judgments tend to produce generic advice.

**Asking for diagnostic questions, not a solution.**
The goal here is not to solve the student's problem with Claude — it is to figure out what to ask the student. Claude cannot know what is going on; only the student can. This is a realistic use of AI as preparation for a conversation, not a substitute for it. The questions Claude suggests are things to try in the meeting; whether they work depends on what the student says.

---

## How to adapt this

**For a struggling postdoc or junior colleague:**
The same structure works. Adjust the language ("a postdoc I am working with" rather than "a student") and the expected level of autonomy. Postdocs are less likely to be avoiding discomfort and more likely to be navigating a genuine problem with project fit or career pressure.

**Before a committee meeting:**
Run this with the student's stated research direction as input and ask Claude: "What are the 3 questions this committee is most likely to push back on, and what would a strong answer to each look like?" Useful for the student to run themselves as preparation.

**When you have a student's self-assessment:**
Paste their self-assessment in place of your observations and ask Claude: "Where might the student's framing of their own situation be a blind spot?" This surfaces the gap between how the student sees the problem and how an outside observer might see it.

**After the meeting:**
If the meeting reveals new information, return to Claude with an update: "Here is what the student said. Which of the explanations fits best now, and what should I do differently in the next meeting?" This turns Claude into a consistent thinking partner across multiple advising conversations.
