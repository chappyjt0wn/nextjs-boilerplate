# Experience Team Complexity Scoring Criteria

## How It Works

Every intake request is scored across 6 dimensions on a 1–3 scale. The total score (6–18) determines whether the request routes to the Express Lane or the Strategy Lane in Monday.

## Scoring Rubric

### 1. Number of Deliverables

| Score | Criteria |
|-------|----------|
| 1 | Single asset (one email, one graphic, one one-pager) |
| 2 | 2–3 related assets (email + social graphic, or a small set) |
| 3 | 4+ assets, or a full campaign suite (emails + landing page + social + print) |

### 2. Strategic Depth Required

| Score | Criteria |
|-------|----------|
| 1 | Template-based or formulaic — clear inputs, known format (e.g., event flyer, internal announcement, bio update) |
| 2 | Requires some creative judgment — messaging angle, audience tailoring, or light concepting needed |
| 3 | Requires full strategic thinking — new positioning, campaign architecture, narrative development, or persuasion strategy |

### 3. Audience Sensitivity

| Score | Criteria |
|-------|----------|
| 1 | Internal audience only (Wellvana employees, internal teams) |
| 2 | Existing partners or providers (known relationship, lower-stakes) |
| 3 | External/new audience, C-suite, regulators, patients, or public-facing (high reputational stakes) |

### 4. Content Originality

| Score | Criteria |
|-------|----------|
| 1 | Repurpose/update existing content — refresh a one-pager, resize a graphic, swap dates on an invite |
| 2 | Adapt existing content for a new context — rewrite for a different audience, restructure for a new channel |
| 3 | Net-new content from scratch — no existing starting point, requires research, interviews, or original writing |

### 5. Stakeholder Complexity

| Score | Criteria |
|-------|----------|
| 1 | Single requestor, no additional approvals needed |
| 2 | 2–3 stakeholders or one additional approval layer |
| 3 | 4+ stakeholders, cross-functional review, legal/compliance review, or executive sign-off required |

### 6. Timeline Pressure

| Score | Criteria |
|-------|----------|
| 1 | Flexible — 3+ weeks, no hard external deadline |
| 2 | Moderate — 1–3 week window, date-driven but some flexibility |
| 3 | Urgent — under 1 week, tied to an immovable event, or already overdue |

## Routing Thresholds

| Total Score | Route | What It Means |
|-------------|-------|---------------|
| 6–9 | **Express Lane** | Simple, repeatable work. AI generates a first draft; a team member reviews, polishes, and ships. Target SLA: 2–3 business days. |
| 10–12 | **Express Lane (Flagged)** | Likely Express, but PM reviews the brief before confirming routing. May escalate to Strategy if the scoring missed nuance. Target SLA: 3–5 business days. |
| 13–15 | **Strategy Lane** | Complex work requiring discovery, creative strategy, and structured timelines. Full PM engagement. Target SLA: 3–4 weeks. |
| 16–18 | **Strategy Lane (High-Touch)** | Campaign-level complexity. Requires dedicated PM, discovery session, stakeholder alignment, and phased delivery. Target SLA: 4–6+ weeks. |

## Scoring Examples

### Example A: "Update the date on the Symposium save-the-date email"
| Dimension | Score | Rationale |
|-----------|-------|-----------|
| Deliverables | 1 | Single asset |
| Strategic depth | 1 | Template update |
| Audience sensitivity | 2 | Existing partners |
| Content originality | 1 | Updating existing |
| Stakeholder complexity | 1 | Single requestor |
| Timeline pressure | 2 | Date-driven |
| **Total** | **8** | **→ Express Lane** |

### Example B: "Build a multi-touch campaign to recruit new ACO partners in the Southeast"
| Dimension | Score | Rationale |
|-----------|-------|-----------|
| Deliverables | 3 | Full campaign suite |
| Strategic depth | 3 | New positioning + persuasion |
| Audience sensitivity | 3 | New external audience |
| Content originality | 3 | Net-new from scratch |
| Stakeholder complexity | 3 | Cross-functional + growth team |
| Timeline pressure | 2 | Moderate (quarterly push) |
| **Total** | **17** | **→ Strategy Lane (High-Touch)** |

### Example C: "Create a one-pager for the Care Management team to share at partner meetings"
| Dimension | Score | Rationale |
|-----------|-------|-----------|
| Deliverables | 1 | Single asset |
| Strategic depth | 2 | Requires audience tailoring |
| Audience sensitivity | 2 | Existing partners |
| Content originality | 2 | Adapting existing messaging |
| Stakeholder complexity | 2 | Requestor + clinical SME |
| Timeline pressure | 1 | Flexible |
| **Total** | **10** | **→ Express Lane (Flagged)** |

## Implementation in Monday

### Board Groups
- **Express Queue** — Items scoring 6–12
- **Strategy Queue** — Items scoring 13–18

### Columns to Add
- **Complexity Score** (number column) — auto-populated by the intake agent
- **Route** (status column) — Express / Express (Flagged) / Strategy / Strategy (High-Touch)
- **Score Breakdown** (long text column) — formatted breakdown of all 6 dimension scores

### Automation Recipes
1. **When Complexity Score changes to 6–9** → Move to Express Queue group, set Status to "Ready for AI Draft"
2. **When Complexity Score changes to 10–12** → Move to Express Queue group, set Status to "PM Review Routing"
3. **When Complexity Score changes to 13–15** → Move to Strategy Queue group, set Status to "Awaiting Discovery"
4. **When Complexity Score changes to 16–18** → Move to Strategy Queue group, set Status to "Awaiting Discovery", notify PM lead

### SLA Tracking
Add a **Due Date** formula column that auto-calculates based on route:
- Express: Creation date + 3 business days
- Express (Flagged): Creation date + 5 business days
- Strategy: Creation date + 21 business days
- Strategy (High-Touch): Creation date + 30 business days
