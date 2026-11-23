## <span style="color:#2F7DDE">Business Analysis Fundamentals with Tableau</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Business Analysis Fundamentals with Tableau"]
  Q["<b>The Big Question</b><br/><i>How do you find the real question before you build the dashboard?</i>"]
  CV["<b>Course use case</b><br/>Analysts map 5 stakeholders and define 1 KPI before opening Tableau on a 90-student dataset"]
  RL["<b>Real-world example</b><br/>A coaching centre owner asks for 'everything' while attendance quietly drops in one batch"]

  CUR ==> Q
  Q ==>|&nbsp;Used in the course&nbsp;| CV
  Q ==>|&nbsp;Seen in real life&nbsp;| RL

  classDef currSes fill:#ffe0b2,stroke:#ef6c00,color:#4e342e,stroke-width:3px
  classDef ask fill:#e3f2fd,stroke:#1565c0,color:#0d47a1,stroke-width:3px
  classDef val fill:#e8f5e9,stroke:#2e7d32,color:#1b5e20

  class CUR currSes
  class Q ask
  class CV,RL val

  linkStyle default stroke-width:3px
```

---

### <span style="color:#2F7DDE">What You'll Learn</span>

Have you ever wondered why a manager asks for "everything" and still feels nothing was answered?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Identify**</span> every person who affects or is affected by a project.
- <span style="color:#D9660B">**Explain**</span> why a quiet stakeholder can block a finished project.
- <span style="color:#D9660B">**Apply**</span> five questions to turn a request into a clear problem.
- <span style="color:#D9660B">**Compare**</span> the request a stakeholder makes with the need behind it.
- <span style="color:#D9660B">**Check**</span> that two analysts would calculate one measure the same way.
- <span style="color:#D9660B">**Design**</span> a one-page brief another person can pick up and use.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> stakeholder mapping, interest and influence quadrants, requirements questions, business need versus proposed solution, KPI design, and one-page documentation.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

The owner of a small coaching centre asks for a dashboard with everything in one place. You build it. Two months later, attendance keeps dropping.

He never opens the dashboard. The reason is simple — it answered a question he never asked.

A <span style="color:#D9660B">**KPI**</span> means one measure with three parts: what it counts, what good looks like, and over what period.

In your course, you will use the same three parts to make sure your dashboards answer the real question.

> <span style="color:#2F7DDE">**Think about it:**</span> Why does a dashboard answering the wrong question still look correct?

---

### <span style="color:#2F7DDE">The Coaching Centre Puzzle</span>

Last month, 90 students were enrolled across five batches.

| Batch | Enrolled | Attending regularly |
|:-----:|:--------:|:-------------------:|
| Morning A | 20 | 16 |
| Morning B | 18 | 10 |
| Evening A | 22 | 19 |
| Evening B | 15 | 7 |
| Weekend | 15 | 12 |

<span style="color:#D9660B">**What you want to happen:**</span>

- See which batch has the lowest attendance.
- Know which two people must agree before you build anything.
- Have the dashboard read the same way to every teacher.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - Why does the owner say "everything" when he might mean one thing?
> - What would make two teachers read the same number differently?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. Which batch needs the most attention?**
Hint: A small batch with few attendees may still have a low rate.

**2. Who else besides the owner might care about these numbers?**
Hint: Think about who sees the students every day.

**3. If two people calculated "attendance rate" differently, what would that look like?**
Hint: One might count students, another might count sessions.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How do you find the real question before you build the dashboard?**</span>
>
> And how can you check two people would answer it the same way?
