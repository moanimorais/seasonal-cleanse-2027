# Seasonal Cleanse 2027 — Workflow Migration

Migration of the **Seasonal Cleanse** automation from 2026 to 2027.

- **Brand:** Live Life With Zest
- **Platform:** All In One Marketing
- **Workflow:** `Seasonal Cleanse 27' Participants Emails & Access Automation`
- **Status:** 🟡 In progress — structure mostly done, content & trigger pending
- **Last updated:** 2026-06-17

---

## Overview

Each year the Seasonal Cleanse program runs a series of cohorts (Winter, Spring ×3, Summer ×3, Fall ×2, possibly more). A single workflow handles three jobs: it **tags** each participant, sorts them into the right **cohort** by date (the "Tagging Divisions" If/else), and sends the **emails + Eventbrite access** for their session.

The 2027 version is built by **copying** the 2026 workflow.

> ⚠️ **Golden rule:** copying only duplicates the structure. Every `2026` value, every `26'` tag, and the enrollment trigger still point to the old year. Anything left at `26'` won't fire in 2027 (the contact falls into the *None* branch). This is an item-by-item review, not a single-date swap.

---

## Progress

```
██████████████░░░░░░  ~70% — structure done, content + trigger remaining
```

### ✅ Done
- [x] Copied and renamed the workflow
- [x] Created the 27' master tag (`seasonal cleanse 27' member`)
- [x] Switched the year to 2027 in Tagging Divisions (1st segment of each branch)
- [x] Created the 10 cohort tags (27')
- [x] Re-pointed the 10 tag actions inside the branches

### ⏳ Pending
- [ ] Re-point the **master tag** action at the top (`Seasonal Cleanse 26' Member` → 27')
- [ ] Verify the **2nd year segment** (below the `OR`) in every branch
- [ ] Fix the **enrollment trigger** in the Settings tab — **critical**
- [ ] Confirm whether a **3rd Fall branch** exists and apply year + tag
- [ ] Decide the **day-of-month** numbers (only if the 2027 calendar differs)
- [ ] Update **emails / Eventbrite links + dates** (depends on the 2027 events existing)
- [ ] Pause the 2026 workflow at the right time
- [ ] Test → Publish

---

## Now vs. Later

> "Depends on 2027" really means "depends on the events existing in Eventbrite." Those can be created ahead of time (e.g. Oct 2026); no need to wait for the year to turn.

| ✅ Can be done now | ⏳ Depends on 2027 events |
|---|---|
| Re-point the master tag at the top | Eventbrite links inside the emails |
| Verify the 2nd year segment in each branch | Dates/times written in the email copy |
| Confirm whether a 3rd Fall branch exists | Day-of-month numbers (only if calendar differs) |
| Fix the trigger (if 2027 source is known) | |

**Plan:** build ~90% now, keep it in **Draft**, then publish branch by branch as each event becomes ready.

---

## Branch control table

`Day` is the current value (from 2026); only change it if the 2027 calendar changes.
`Year (both)` = confirm **both** segments (above and below the `OR`) read 2027.

| Branch | Segment 1 (month / day) | Segment 2 OR (month / day) | Year (both) | 27' tag | Action re-pointed |
|---|---|---|:---:|:---:|:---:|
| 1st Winter | Jan | Feb / on or before 6 | ⬜ | ✅ | ✅ |
| 1st Spring | Feb / on or after 13 | Apr / on or before 10 | ⬜ | ✅ | ✅ |
| 2nd Spring | Apr / on or after 17 | May / on or before 8 | ⬜ | ✅ | ✅ |
| 3rd Spring | May / on or after 15 | Jun / on or before 5 | ⬜ | ✅ | ✅ |
| 1st Summer | Jun / on or after 12 | Jul / on or before 10 | ⬜ | ✅ | ✅ |
| 2nd Summer | Jul / on or after 17 | Aug / on or before 7 | ⬜ | ✅ | ✅ |
| 3rd Summer | Aug / on or after 14 | Sep / on or before 11 | ⬜ | ✅ | ✅ |
| 1st Fall | Sep / on or after 18 | Oct / on or before 9 | ⬜ | ✅ | ✅ |
| 2nd Fall | Oct / on or after 16 | Nov / on or before 6 | ⬜ | ✅ | ✅ |
| 3rd Fall (?) | check in workflow | check | ⬜ | ⬜ | ⬜ |

> The `Year (both)` column is intentionally unchecked: the year was switched, but the **2nd segment** of each branch still needs the verification pass.

---

## Notes & don'ts

- **Do not touch** `Current month` or `Current Day of month` values — they define the cohort calendar. The only change in those segments is the **year** (unless the 2027 schedule differs).
- The **trigger** is the most commonly missed item. A copied workflow keeps the 2026 enrollment source; if not updated, 2027 enrolls no one.
- Keep the workflow in **Draft** until the 2027 Eventbrite links are live.

## Open questions

- [ ] Does a **3rd Fall branch** (and/or a Dec/Jan wrap-up) actually exist? Screenshots were cut off.
- [ ] Are the Eventbrite links in the emails **fixed (typed in)** or **dynamic (custom value / merge field)**? Decides whether the email update is quick or tedious.
