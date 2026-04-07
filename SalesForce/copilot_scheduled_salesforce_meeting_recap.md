---
title: SalesForce Meeting Recap
description: "This iteration of the SalesForce Meeting Recap prompt is used to create a scheduled prompt that runs at 5PM each business day to "
tags:
    - SalesForce
    - Scheduled Prompt
    - Transcripts
related_tools:
    - Copilot
isPrivate: false
frequency:
    - On Demand
    - Daily
when: 5:00 PM
---

TASK:
Generate Salesforce-ready meeting notes for meetings on my calendar that occurred since 5:00 PM ET of the prior business day (if today is Monday, look back to Friday at 5:00 PM ET).

TIME WINDOW (ET):
- StartTime = 5:00 PM ET on the prior business day
- EndTime = Today at 5:00 PM ET
- Include meetings whose start time falls within [StartTime, EndTime]

MEETING EVALUATION:
Evaluate meetings from my calendar within the time window.

INCLUDE a meeting if ANY are true:
- At least one attendee other than me is invited, OR
- <tmaloney@lazy-jamrock.com> is NOT on the attendee list, OR
- There is evidence of collaboration (meeting transcript, recap, recording, or substantive meeting chat)

EXCLUDE (skip) a meeting if ALL are true:
- No one else is invited (solo meeting), AND
- No transcript, recap, recording, or substantive chat exists, AND
- It appears to be a personal block (e.g., Focus Time, Hold, Blocked, OOO, Travel, Admin)

Solo personal blocks with no collaboration evidence are always skipped.

SOURCE PRIORITY (GROUND TRUTH):
For each included meeting, summarize using sources in this strict order:
1) Meeting transcript
2) Meeting recap
3) Meeting chat
4) Meeting invite (title, agenda/description, attendees, organizer)

If no transcript exists:
- Keep summaries conservative and grounded only in chat or invite details
- Do NOT infer specifics not explicitly stated

INTERNAL TITLE RULE:
If a meeting is purely internal (all attendees are Protiviti or Robert Half; no external participants):
- Prefix the title with: INTERNAL -

If internal vs external status is ambiguous, do NOT apply the prefix.

EDITED-LIKELY MARKER (REQUIRED):
For each meeting, include an Edited‑Likely marker with a short reason (3–10 words):
- Edited‑Likely: Low → Transcript exists or recap is detailed
- Edited‑Likely: Medium → No transcript, but substantive chat or clear invite agenda
- Edited‑Likely: High → No transcript, minimal chat, little or no invite detail

OUTPUT FORMAT (STRICT):
- Plain text only
- Use "- " for all bullets
- Chronological order (oldest to newest)
- One meeting note per included meeting
- Do NOT add commentary outside the defined structure

DIGEST HEADER:
Daily Meeting Notes Digest (ET): <StartTime> to <EndTime>
Meetings included: <count>

FOR EACH MEETING, OUTPUT EXACTLY:

Edited‑Likely: <Low | Medium | High> (<short reason>)
Title: <5–10 word meeting description>
(If internal: Title: INTERNAL - <5–10 word meeting description>)

Body:
2–3 sentences summarizing meeting intent and high-level topics using the highest-priority source available.

OPPORTUNITIES:
- <Short title (≤7 words)> [Confidence: High | Medium | Low]: <One sentence describing a significant consultative work effort>
(Max 7 bullets; omit OPPORTUNITIES entirely if none are supported)

FOLLOW-UPS:
- <Contact Name>: <One sentence describing follow-up topic>
(Max 5 bullets; omit FOLLOW-UPS entirely if none are supported)

OPPORTUNITY QUALITY RULES:
Only include strategic, multi-step efforts such as:
- Assessments or maturity reviews
- Program or process redesign
- Operating model or transformation initiatives
- Managed services or programmatic security testing

Exclude tactical one-offs (minor fixes, simple configuration changes, or tasks the client would reasonably perform themselves).
It is acceptable for a meeting to have zero opportunities.

CONFIDENCE SCORING:
- High: Explicit request for help/proposal/scope/timing/owner/budget; dissatisfaction with a provider
- Medium: Clear gap acknowledged; exploratory questions; interest without commitment
- Low: Implied or vague; no urgency or ownership
When uncertain, choose the lower confidence or omit the opportunity.

SELF-IMPROVEMENT LOOP (REQUIRED):
After the digest, ask exactly once:

“Please paste the final version(s) of any meeting notes you entered into Salesforce today that you edited (only the edited ones). If you changed something significantly, add a short phrase on why.”

When edited notes are provided:
1) Summarize changes at a high level
2) Identify 1–3 repeatable preference rules implied by the edits
3) Output a section titled PROMPT PATCH containing only new or modified instruction lines to add to this prompt
4) Ask at most ONE targeted clarification question if a preference is unclear

Do NOT assume preferences persist automatically—always output explicit prompt patches suitable for copy/paste.