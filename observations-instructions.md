# Tim's Observation Review Coach Agent

## Purpose of This Tool

This LLM is designed to act as a **senior IT risk, governance, and enablement reviewer and writing coach**. It helps you draft clear, precise, and defensible observations based on a capability maturity model or similar framework.

It is not a content generator you hand work off to. It is a **guided drafting partner** that will challenge vague thinking, ask clarifying questions, and help you iterate toward a strong observation.

The goal is to produce one high-quality observation at a time that aligns with our observation writing guide and review rubric.

## Setting up ProGPT
1. Navigate to [my GitHub Repository](https://github.com/lazyshamrock/Work-Templates/blob/main/observations-prompt.txt) and copy the text content to the clipboard.
2. Navigate to ProGPT and create a new chat.
2. Click on the Persona button at the top of the chat window.
3. Click the Edit button to edit the persona.
4. Paste the prompt text into the Persona text box.
5. Click Save Persona and add a name for the persona.

You can now reuse this persona in any chat going forward.

## The Basic Workflow

The tool follows a structured conversation. You do not need to memorize it, but understanding the flow will make it easier to use.

### Step 1: Provide the Expected Maturity Attribute

Start by pasting the maturity attribute you are assessing, or describe the expected capability in your own words.

Examples:

- Pasting the attribute directly from the maturity model
- Summarizing the attribute in plain language

If the expectation is unclear, the tool will stop and ask questions. This is intentional.

### Step 2: Describe What Was Observed

Explain what was missing, incomplete, or unevenly applied.

Include:

- Where the capability exists
- Where it does not exist
- Any known inconsistencies

When in doubt, provide more detail. It is easier to shorten later than to add context back in.

### Step 3: Share Evidence or Signals

Describe any evidence that supports the gap, such as:

- Interview feedback
- Missing or incomplete documentation
- Observable behaviors tied to the attribute

If no clear evidence was observed, say so. The tool will proceed but may suggest follow-up questions.

### Step 4: Discuss Impact or Risk

Explain why the gap matters.

If your risk statement is vague, the tool will propose several alternative risk framings for you to choose from or refine. Select the one that best reflects your intent, or provide your own.

### Step 5: Review the Working Draft

The tool will produce a **working draft observation** as a single paragraph.

You should:

- Read it critically for accuracy
- Confirm it reflects what you observed
- Check that the impact feels fair and precise

The draft is not final until you are comfortable with it.

### Step 6: Iterate or Move On

After reviewing the draft, you can:

- Ask the tool to refine specific parts
- Add missing details or examples
- Confirm the observation and move on to the next attribute

Iteration is expected. Do not try to perfect everything in one pass.

## How the Tool Will Coach You

You should expect the tool to:

- Stop you when language is vague or interpretive
- Ask clarifying questions before drafting
- Explain why certain wording works or does not work
- Reference the internal review rubric when giving feedback

This mirrors how observations are reviewed during internal quality review.

## Asking for Help

At any point, you can ask questions such as:

- "How should I phrase this?"
- "Why is this wording risky?"
- "Can you explain how to use this tool?"

The tool can switch into an explanatory mode and then return to drafting when you are ready.

## Key Reminders

- This tool helps you think and write more clearly. It does not replace judgment.
- Write more in early drafts and refine through iteration.
- Assume gaps exist if no evidence was observed; stakeholders will validate later.
- If something feels unclear, ask questions early rather than guessing.

Used well, this tool should reduce rework, improve consistency, and make review conversations more productive.