# Tim’s Observation Review Coach Agent

## Purpose of This Tool

This LLM is designed to act as a **senior IT risk, governance, and enablement reviewer and writing coach**. It helps you draft clear, precise, and defensible observations based on a capability maturity model or similar framework.

It is not a content generator you hand work off to. It is a **guided drafting partner** that will challenge vague thinking, ask clarifying questions, and help you iterate toward a strong observation.

The goal is to produce one high-quality observation at a time that aligns with our observation writing guide, drafting checklist, and lightweight review rubric.

---

## Prompt Revision History
- 2025-12-18: Initial Publication
- 2025-12-19: Added Process Reflection and Continuous Improvement process to prompt to enable future enhancements.
- 2025-12-19: Incorporated revisions based on feedback from first use.

## Setting up ProGPT

1. Navigate to my GitHub repository and copy the prompt text:  
   https://github.com/lazyshamrock/Work-Templates/blob/main/observations-prompt.md?plain=1
2. Navigate to ProGPT and create a new chat.
3. Click the **Persona** button at the top of the chat window.
4. Click **Edit** to modify the persona.
5. Paste the prompt text into the Persona text box.
6. Click **Save Persona** and give it a recognizable name.

You can now reuse this persona in any chat going forward.

---

## The Basic Workflow

The tool follows a structured conversation. You do not need to memorize it, but understanding the flow will make it easier to use and easier to iterate.

### Step 1: Provide the Expected Maturity Attribute

Start by pasting the maturity attribute you are assessing, or describe the expected capability in your own words.

Examples:
- Pasting the attribute directly from the maturity model
- Summarizing the attribute in plain language

If the expectation is unclear, the tool will stop and ask questions. This is intentional and part of the coaching process.

---

### Step 2: Describe What Was Observed (Current State Only)

Explain what was missing, incomplete, or unevenly applied **today**.

Include:
- Where the capability exists
- Where it does not exist
- Any known inconsistencies

Avoid references to future plans, roadmaps, or intended improvements unless they are essential to understanding the current gap.

When in doubt, provide more detail. It is easier to shorten later than to add context back in.

---

### Step 3: Share Evidence or Signals

Describe any evidence that supports the gap, such as:
- Interview feedback
- Missing or incomplete documentation
- Observable behaviors tied to the attribute

If no clear evidence was observed, say so. The tool will proceed but may suggest follow-up questions or areas to confirm.

---

### Step 4: Discuss Impact or Risk

Explain why the gap matters.

The tool will help frame risk using a simple lens, such as:
- Operational inefficiency
- Compliance or regulatory exposure
- Strategic misalignment

If your initial risk statement is vague, the tool will propose example risk framings and ask you to confirm or adjust them.

---

### Step 5: Review the Working Draft

The tool will produce a **working draft observation** as a single paragraph.

You should:
- Read it critically for accuracy
- Confirm it reflects what you observed
- Check that the impact feels fair, precise, and defensible

The draft is not final until you are comfortable with it.

---

### Step 6: Iterate or Move On

After reviewing the draft, you can:
- Ask the tool to refine specific parts
- Add missing details or examples
- Confirm the observation and move on to the next attribute

Iteration is expected. Do not try to perfect everything in one pass.

---

## Process Reflection and Continuous Improvement

This tool also supports a **process reflection step** to help continuously improve how observations are drafted and reviewed.

### When to Use Reflection

Trigger reflection when:
- You complete an observation or a set of observations
- You notice recurring friction, confusion, or rework
- You want to improve the prompt, checklist, rubric, or workflow itself

### How to Trigger Reflection

In the chat, enter either:
- `\reflect`
- `\complete`

This signals that drafting is done and that the tool should shift from coaching to reflection.

### What Reflection Does

When reflection is triggered, the tool will:
1. Summarize what worked well and what could improve in the drafting process
2. Identify which guidance components may need updates (e.g., prompt instructions, drafting checklist, review rubric)
3. Propose specific edits in Markdown format suitable for direct inclusion
4. Ask follow-up questions if clarification or approval is needed

This reflection is about **improving the system**, not revising past observations.

### Call to Action

If the reflection proposes changes that feel useful:
- Copy the suggested edits
- Send them back to Tim for review
- Approved updates will be incorporated into the master prompt and supporting documentation

Do not assume changes are adopted until they are reviewed and incorporated centrally.

---

## How the Tool Will Coach You

You should expect the tool to:
- Stop you when language is vague or interpretive
- Ask clarifying questions before drafting
- Provide concrete examples when refining impact language
- Reference the internal review rubric when explaining feedback

This mirrors how observations are reviewed during internal quality review.

---

## Asking for Help

At any point, you can ask questions such as:
- “How should I phrase this?”
- “Why is this wording risky?”
- “Can you explain how to use this tool?”

The tool can switch into explanation mode and then return to drafting when you are ready.

---

## Key Reminders

- This tool supports thinking and writing. It does not replace judgment.
- Write more in early drafts and refine through iteration.
- Assume gaps exist if no evidence was observed; stakeholders will validate later.
- If something feels unclear, ask questions early rather than guessing.
- Reflection is part of the process, not extra work.

Used well, this tool should reduce rework, improve consistency, and steadily improve both observation quality and the drafting process itself.
