Here is the **Project Memory** document customized for your repository (`kasina-curriculum`). 

You can save this as a file (e.g., `PROJECT_MEMORY.md` or just keep it in your local notes) so that any AI assistant or team member knows the exact rules for your batches.

***

# Project Memory: Curriculum Pipeline (`kasina-curriculum`)

> **Workspace Role**: You are assisting SME / Curriculum Creator Kasina in developing 120-minute lecture scripts (`lecture-script.md`) and learner pre-reads (`pre-read.md`).

---

## 1. Active Batches & Curriculum Sources

All sessions, learning objectives, and prerequisite contexts come directly from the batch CSVs in `curriculum/`:

| Batch ID | Program | Curriculum CSV |
|:---|:---|:---|
| **`iitreict-dsai-2605`** | Certification in Data Science & AI | `curriculum/iitreict-dsai-2605.csv` |
| **`iimrc-baai-ii-2607`** | Executive Programme in Business Analytics & AI | `curriculum/iimrc-baai-ii-2607.csv` |
| **`iimrc-ba-en-iii-2609`** | Executive Programme in Business Analytics (EN) | `curriculum/iimrc-ba-en-iii-2609.csv` |
| **`we-da-te-ii-2609`** | Data Analytics (Tech Executives) | `curriculum/we-da-te-ii-2609.csv` |

---

## 2. Directory & File Structure Rules

* **Batch Root**: `<batch-id>/`
* **Module Folders**: `module-<NN>-<topic-slug>/` (lowercase, zero-padded, hyphens only).
* **Lecture Folders**: `lecture-<NN>-<topic-slug>/` sequentially numbered per module.
* **Mandatory Files Per Lecture**:
  * `pre-read.md` (student self-study guide before session)
  * `lecture-script.md` (120-minute mentor teaching script)
  * `images/` (only when the script includes charts, PNG 900px wide, dpi 200)
  * `data/` (only when the script uses datasets, 100-150 rows with edge cases)
* **Zero Bloat**: No `.gitkeep` files, no temporary or leftover scripts.

---

## 3. Mandatory Generation Guardrails

Every time a pre-read or lecture script is created or edited, strictly enforce:

### Guardrail 1: Zero Jargon (High Accessibility)
* Write as an approachable, empathetic senior mentor talking to a colleague.
* Grade 7 reading level; plain, simple, human English.
* **Intuition first**: Explain *why* a concept exists using concrete everyday analogies before showing code, formulas, or syntax.
* Never use ungrounded academic abstractions, buzzwords, or textbook jargon. If a technical term is essential, define it once in plain English immediately upon introduction.
* Banned buzzwords: `leverage`, `utilize`, `robust`, `seamlessly`, `empower`, `cutting-edge`, `dive into`, `delve`.

### Guardrail 2: Strict Curriculum Alignment (Prerequisite Hard-Boundary)
* Cross-reference `curriculum/<batch_id>.csv` before drafting.
* Content, examples, code, and quiz questions must be generated **strictly based on the sessions already completed**.
* **Do NOT introduce, assume, or reference topics that haven't been taught yet.**
* Check all code libraries, functions, and SQL syntax: if it is neither part of today's LOs nor taught in previous sessions, it is strictly banned.
* **Zero forward references**: Never write "more on this in later modules", "we will cover this next week", or preview upcoming topics.

### Guardrail 3: Mandatory Real Data, Visuals, and Closing Structure
* **Dataset (`data/`)**: Always include a 100-150 row CSV dataset in `data/` with realistic planned edge cases (duplicates, missing values, spaces, casing). Code starts with rows 1-10 and scales to all rows in Topic 4/Closing.
* **Visuals (`images/`)**: Always generate 5-6 real PNG charts/diagrams (900px wide, dpi 200) in `images/` embedded with `<p align="center"><img src="images/XX_name.png" alt="..." width="900"></p>`.
* **Closing Elements**: Must include Outcome comparison table (Before vs After), `Therefore,` deduction, Opening Poll reveal note, Summary table with `Practical value`, and `# <font color='red'>Launch the Feedback Poll</font>` with Reminder instructor note.
* **Agenda Format**: Closing row must use `—` marker (`| — | Closing: Outcome & Summary | | MIN |`) with total summing to `**120**`. Only 🎯 emoji is allowed.

---

## 4. Templates

* **Lecture Script Template**: `templates/lecture-script-template.md` (Frozen Format v2).
  * Structure: Agenda (sums to 120 min) -> Scenario (famous Indian company framing) -> Problem Statement -> What We Will Use -> How (Mermaid flow) -> Topics 1 to 4 (Bridge Question, Example, Extending it, Quiz) -> Closing: Outcome & Summary -> Announcements -> Launch the Feedback Poll.
* **Pre-Read Template**: `templates/pre-read-template.md`.
  * Structure: Mental Map (Mermaid flowchart) -> What You'll Learn (Bloom's verbs) -> Core Concepts -> Scenario Puzzle -> Think It Through (3 questions with hints, no answers) -> One Question to Carry -> Setup.

---

## 5. Execution Commands & Helper Tools

When generating or verifying scripts:
```bash
# 1. Resolve target lecture directory
python3 tools/resolve_folder.py "<BATCH-ID>" "<Session Name>"

# 2. Check completed curriculum context
python3 lecture/tools/curriculum_context.py "curriculum/<BATCH-ID>.csv" "<Session Name>"

# 3. Deterministic checker for lecture script structure, minutes, quizzes, and terms
python3 lecture/tools/check_script.py <path/to/lecture-script.md> --los "<LO1;LO2>" --announcements no
```
