# Prompt-first writes to a shared calendar

## PATTERN

Approval-gated writes to shared state. An automated catcher may read everything, but it writes nothing to a shared surface without the principal's explicit approval. Candidates collect in a pending file and are decided in one batch reply: all / some / none.

## CONTEXT

A two-adult household runs on one shared calendar. Mail, school notices, team apps, and group chats all carry dated items, and anything not on the calendar effectively does not exist for the household — so missed items are costly. But an agent writing events uninvited is costlier: one wrong auto-added entry trains the humans to distrust every entry on the calendar.

## CONFIG

- A catcher scans inboxes and message sources on a daily pass, deduped by watermark so a seen item never resurfaces as a candidate.
- Each candidate lands in a pending-approvals file with its source, its date, and the exact event that would be created.
- The principal approves all / some / none in a single reply. Events are created only after that approval, with the other adult copied on anything family-affecting.
- One pre-approved class bypasses the queue: school dress-up and theme days are created directly and merely noted in the report. The class is narrow, named, and revocable.

## RESULT

In the first audit under this regime, 41 duplicate feed copies of events were found on the primary calendar and removed; the shared family calendar became the canonical copy. Since the gate went in: zero unapproved writes, and the batch approval takes the principal under a minute.

## FAILURE MODES

- Approval fatigue: if the pending file grows noisy, the principal starts rubber-stamping. Keep candidates household-relevant; log the filtered-out items instead of asking about them.
- Silent drops: an item carrying a date, deadline, cost, or bring/wear instruction must never be dropped quietly. If it fails the relevance test, it still surfaces as a one-line heads-up.
- Exception creep: the pre-approved class must stay narrow and named, or the gate becomes decorative.

## TRANSFER

Any automation that writes to a surface other people trust — shared calendars, shared inboxes, team boards, family chats. Read freely; write only through a gate the principal can audit.
