# Learning Playbook — How to Learn by Building with an AI Coding Agent

You're starting from **zero C++ and ROS 2 knowledge**. This project builds both from scratch. The code we write is practice, not product — every interaction should leave you with a clearer mental model, not just working binaries.

---

## Mindset

You're not here to *get a working robot arm*. You're here to *become someone who could build a robot arm yourself*. The AI is a pair programmer and tutor — not a code generator.

**Core principle:** You drive, the AI navigates. You make the decisions, the AI asks questions that help you see the path.

---

## How Each Session Should Flow

### 1. State your intent
> *"Let's start Phase 0 — I want to set up Docker and compile hello-world C++."*

The AI will then ask 2-3 scaffolding questions before any code is written. This is normal — it's the learning starting.

### 2. Expect questions, not answers
When you say "let's build Vector3D", the AI will ask:
- *"What operations should a 3D vector support?"*
- *"Should cross() return a new vector or modify in place?"*
- *"How would you test normalize()?"*

**The goal:** you think through the design first. The code writes itself after that.

### 3. Pick a mode

| Mode | When to use | What happens |
|------|------------|--------------|
| **Explain mode** | You want to understand a concept first | AI describes the concept, you write the code |
| **Show me** | You want to see the pattern once | AI writes with line-by-line narration, then you do the next one |
| **Review this** | You wrote code and want feedback | AI critiques correctness, style, edge cases |

### 4. Ask "why?" freely
If something doesn't click, say so:

| Instead of nodding along | Say this |
|---|---|
| *(silence)* | **"Why does this line need `const &`?"** |
| *(accepting magic)* | **"What's the mental model here?"** |
| *(moving on)* | **"I don't fully get X. Can we go over it?"** |

There are no stupid questions. If something looks like boilerplate, there's usually a reason — ask.

### 5. Use the checkpoint test
Before moving to the next step, you should be able to explain:

1. What each file does and why it exists
2. How the build system connects them
3. What each Docker layer contributes
4. The key concept you just learned

If you can't explain it, the step isn't done. Say: **"I'm fuzzy on X — let me try to explain it, correct me where I'm wrong."**

---

## Conversation Patterns That Work

### Starting a task
> *"I want to build the Vector3D class from Step 1.1."*

The AI will respond with guiding questions. Your answers shape the code — there's no single "right" answer.

### When stuck on an error
1. Read the error message — what file, what line, what type of error?
2. Try to guess what's wrong before asking
3. Then say: *"I got this error. I think it means X, but I'm not sure. Help?"*

### When you're unsure
> *"I think this is right because X — am I missing anything?"*

This shows you're thinking, and the AI can confirm or correct your mental model.

---

## Anti-Patterns to Avoid

| Instead of | Try |
|---|---|
| "Write the Dockerfile for me" | "What's the minimal Dockerfile for this? Walk me through each line." |
| "Is this right?" | "I think this is right because X — am I missing anything?" |
| "What's next?" | "I'm comfortable with this step. Here's what I learned: (explain). Let's move on." |
| (pasting errors without reading them) | Read the error, find the line it points to, then ask |

---

## When You Get Stuck (You Will)

That's the best learning moment. Algorithm:

1. **Read the error** — find the file, line number, and error type
2. **Guess** — what do you think is wrong?
3. **Ask** — "I got this error. I think it means X, help?"

The AI will explain the *concept* behind the error, not just the fix.

---

## Be Honest About Your Comfort Level

If the AI asks "ready to move on?" and you're not — **say so**. The roadmap is a guide, not a deadline. We can:

- Do a second pass on the current step
- Add a mini-exercise to make it stick
- Try a different angle on the same concept

---

## Quick Reference Card

```
YOUR GOAL: understanding, not code output
YOUR JOB:  design decisions, headers, tests, "why" questions
AI'S JOB:  guide with questions, explain concepts, fill boilerplate, review

Three modes:
  "Explain mode" — teach me first, then I write
  "Show me"     — show me once (with narration), then I do
  "Review this" — I wrote it, what do you think?

Checkpoint: can I explain each file's purpose? Good? Move on. No? Stay.
```
