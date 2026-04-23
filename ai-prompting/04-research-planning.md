# Example 4: Planning a Research Task Before Starting It

---

## Research context

I am starting a new project phase: collecting and processing LiDAR scans of a historic church to build a damage detection model. I have a general idea of what I want to accomplish and a rough timeline in my head, but I know from experience that scope and data requirements for this kind of work are easy to underestimate. I want to think it through carefully before committing to a plan.

---

## The prompt

```
I am planning a research task and want to think it through before committing to a
timeline. I will describe what I want to accomplish. Your job is not to give me a plan —
it is to help me surface what I have not thought through yet.

The task: I want to collect LiDAR scans of a historic masonry church, process the point
clouds into a usable 3D model, and use the geometry to train a model that detects
structural damage patterns. The goal is a methodology paper with results from one
building, completed within 8 months.

Ask me 5 questions — the most important things I need to decide or know before I can
write a realistic plan. Do not ask about things I have already answered above. After I
answer, we will build the plan together.
```

---

## Why I structured it this way

**"Your job is not to give me a plan."**
This is the key instruction. If you leave it out, Claude immediately produces a generic project plan with phases, milestones, and deliverables. It looks complete but it is built on assumptions about your resources, constraints, and context that are almost certainly wrong. Suppressing the plan forces Claude into a different mode — asking rather than answering.

**Asking for questions first.**
The questions Claude asks reveal what is underspecified in your framing. Common ones for fieldwork-heavy projects include: Do you have site access confirmed? What is your ground truth for "damage"? How will you handle scan registration across sessions? These are things you may have thought about, or may not have — either way, surfacing them before you commit to a timeline is valuable.

**"After I answer, we will build the plan together."**
This sets up an iterative conversation. Research planning is a dialogue. If you frame it as a single prompt-and-response, the output is less useful than if you treat it as a back-and-forth where Claude's questions inform the plan.

**Limiting to 5 questions.**
Without a number, Claude asks 10 to 15 questions, which is too many to engage with at once. Five is a manageable number that still forces prioritization. If the first five answers raise new questions, Claude will surface them in the next round.

**Including a concrete description.**
The more specific your description of the task, the better the questions. "I want to do 3D analysis of a building" produces generic questions. "LiDAR scans of a historic church, point cloud processing, damage detection, methodology paper, 8 months" produces specific ones about scan density, model architecture, ground truth labeling, and publication timeline.

---

## How to adapt this

**For experiment design:**
Use the same structure but change the framing: "I am designing an experiment to test whether [X]. Your job is to help me surface what I have not decided yet." After you answer the questions, add: "Also flag potential confounds I should account for in the design."

**For a student planning their dissertation chapter:**
Run this conversation with the student present, or ask the student to run it themselves and bring the output to your meeting. Watching them answer Claude's questions often reveals assumptions they have not articulated — which is exactly what you need to know before they spend two months going in the wrong direction.

**For semester or lab planning:**
Works at a coarser scale. Describe your lab's goals for the semester and ask Claude to identify dependencies or sequencing problems before you assign tasks. Useful when multiple students are working on connected pieces.

**Following up after the questions:**
Once you have answered Claude's five questions, say: "Now, based on my answers, draft a project plan with phases, key decisions, and risks. Flag any remaining unknowns explicitly." This produces a plan grounded in your actual constraints rather than generic assumptions.
