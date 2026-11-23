## <span style="color:#2F7DDE">Insight Communication & Storytelling with Tableau</span>

### <span style="color:#2F7DDE">Mental Map</span>

```mermaid
%%{init: {'flowchart': {'nodeSpacing': 45, 'rankSpacing': 55, 'padding': 20}}}%%
flowchart TB
  CUR["<b>Current Session</b><br/>Insight Communication &amp; Storytelling with Tableau"]
  Q["<b>The Big Question</b><br/><i>How do you turn a chart into a decision someone will act on?</i>"]
  CV["<b>Course use case</b><br/>Analysts turn a 200-row sales sheet into a one-page story a manager acts on in five minutes"]
  RL["<b>Real-world example</b><br/>A phone shop manager explains which model keeps coming back for repairs"]

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

Have you ever wondered why some charts get acted on and others get ignored?

By the end of this session, you will be able to:

- <span style="color:#D9660B">**Identify**</span> the decision your reader is about to make.
- <span style="color:#D9660B">**Explain**</span> what each of the four story parts does for the reader.
- <span style="color:#D9660B">**Interpret**</span> which chart carries a message fastest.
- <span style="color:#D9660B">**Apply**</span> the four-part order to one finding in Tableau.
- <span style="color:#D9660B">**Check**</span> that a written note names an owner and a date.
- <span style="color:#D9660B">**Design**</span> a one-screen story a manager can follow alone.

> <span style="color:#2F7DDE">**Topics you will meet:**</span> audience-first framing, chart choice by message, headline–context–insight–recommendation, Story Points and annotations, and written handover notes.
>
> Join the session to learn each of these in detail.

---

### <span style="color:#2F7DDE">Why You Are Learning This Topic</span>

You run a small phone shop. Last month, 40 phones came back for repairs.

You know the number. Your area manager does not.

If you send a chart alone, she will ask "so what?" If you send four lines with a clear next step, she will answer in ten minutes.

A <span style="color:#D9660B">**story**</span> means four parts — headline, context, insight, recommendation — in that order.

In your course, you will use the same four parts on every dashboard you build.

> <span style="color:#2F7DDE">**Think about it:**</span> Why does one chart get a reply and another get silence?

---

### <span style="color:#2F7DDE">The Phone Shop Puzzle</span>

These are last month's sales and returns from one shop.

| Model | Units sold | Units returned |
|:-----:|:----------:|:--------------:|
| Nova X | 120 | 6 |
| Orbit 5 | 80 | 32 |
| Pulse 3 | 60 | 4 |
| Edge 9 | 40 | 2 |
| Mini 7 | 50 | 3 |

<span style="color:#D9660B">**What you want to happen:**</span>

- Show which model is returned far more than the others.
- Make the gap visible in two seconds, not two minutes.
- Give the area manager one clear next step with a name and date.

> <span style="color:#D9660B">**Wonder about this:**</span>
>
> - Why does a table of five rows hide the problem better than a sorted chart?
> - What would the area manager do first if you only sent the numbers?

---

### <span style="color:#2F7DDE">Think It Through</span>

There is no wrong first try. Keep your guesses for the session.

**1. Which model would you lead with in your first sentence?**
Hint: Compare returns against units sold, not returns alone.

**2. What does the area manager need to decide after reading your note?**
Hint: Think about what she can actually change this month.

**3. What would you put in the last line of your note?**
Hint: A decision needs someone to own it and a date to check it.

---

### <span style="color:#2F7DDE">One Question to Carry Into the Session</span>

> <span style="color:#2F7DDE">**How do you turn one chart into a decision someone will act on?**</span>
>
> And how can you check your story reads clearly without you in the room?
