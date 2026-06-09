# CourseFiles — Course Design Documents

One `.md` file per course, produced by the [Course Design Workflow](../Course_Design_Workflow.md) and
verified against the [Course Design Checklist](../Course_Design_Checklist.md).

---

## Folder map

```
CourseFiles/
├── Foundation/    ← courses common to all engineering programs (Sem I–II basics + mandated subjects)
├── CS-Core/       ← courses common across SoCSE programs (CS fundamentals shared by 2+ programmes)
├── AIDS/          ← AIDS-specific + AIDS+AIML shared courses (same code → one canonical file)
├── AIML/          ← AIML-exclusive courses (AIDS+AIML shared courses are filed under AIDS/)
├── CSE/           ← CSE-exclusive courses
├── CSIT/          ← CSIT-exclusive courses
├── ISE/           ← ISE-exclusive courses
└── IoT/           ← IoT-exclusive courses
```

**Placement rule — one file per unique course code, in the most general applicable folder:**

| Where it goes | Condition |
|---|---|
| `Foundation/` | Non-CS-specific: maths, sciences, engineering basics, English, ethics, constitution |
| `CS-Core/` | CS-specific content shared by 2 or more SoCSE programmes |
| `<PROGRAM>/` | Unique to one programme (or a small cluster; canonical copy in the primary programme folder) |

---

## Current course file inventory

### Foundation/ — 15 files

| File | Course | Programmes | Sem |
|---|---|---|---|
| CF_B24AS0103_... | Multivariable Calculus and Linear Algebra | All 6 | I |
| CF_B24AS0105_... | Chemical Technology for Computing | AIDS, AIML | I |
| CF_B25AS0105_... | Chemical Technology for Computing | CSE, CSIT, ISE, IoT | II |
| CF_B25EE0101_... | Electronics and Digital Logic | All 6 | I |
| CF_B25EE0102_... | Electronics and Digital Logic Lab | All 6 | I |
| CF_B24ED0102_... | Fundamentals and Applications of Civil Engineering | All 6 | I |
| CF_B24EN0102_... | Finance and Management | All 6 | I |
| CF_B24AS0203_... | Probability and Statistics | All 6 | II |
| CF_B24AS0106_... | Physics for Computer Science | All 6 | II |
| CF_B24AS0108_... | Physics for Computer Science Lab | All 6 | II |
| CF_B24ME0105_... | Fundamentals of Mechanical Engineering | All 6 | II |
| CF_B24ME0102_... | Innovation and Entrepreneurship | All 6 | II |
| CF_B24AH0103_... | Communicative English | All 6 | II |
| CF_B25AS0301_... | Discrete Mathematics and Graph Theory | AIDS, AIML, CSE | III |
| CF_B25ME0301_... | Indian Constitution and Cyber Law | AIDS, AIML, CSE | III |

### CS-Core/ — 14 files

| File | Course | Programmes | Sem |
|---|---|---|---|
| CF_B24CI0109_... | Introduction to C Programming | AIDS, AIML | I |
| CF_B24CI0110_... | Introduction to C Programming Lab | AIDS, AIML | I |
| CF_B25CI0101_... | Introduction to C Programming | CSE, CSIT, ISE, IoT | I |
| CF_B25CI0102_... | Introduction to C Programming Lab | CSE, CSIT, ISE, IoT | I |
| CF_B25CS0101_... | Python for Data Science | All 6 | I |
| CF_B25CS0102_... | Python for Data Science Lab | All 6 | I |
| CF_B25CS0201_... | Business Analysis and Software Design | All 6 | II |
| CF_B25CI0201_... | Advanced C Programming with Generative AI | All 6 | II |
| CF_B24EN0101_... | Internet of Things | All 6 | II |
| CF_B25CI0203_... | Grand Challenge (Extra Credit, Optional) | All 6 | II |
| CF_B25CS0301_... | Data Structures and Algorithms | AIDS, AIML, CSE | III |
| CF_B25CS0302_... | Data Base Management Systems | AIDS, AIML, CSE | III |
| CF_B25CS0304_... | Introduction to Design Thinking | AIDS, AIML, CSE | III |
| CF_B25CS0305_... | AEC-1 (Placement Training) | AIDS, AIML, CSE | III |

### AIDS/ — 4 files (all also cover AIML — same course code)

| File | Course | Programmes | Sem |
|---|---|---|---|
| CF_B25EA0301_... | Object Oriented Programming with Python | AIDS, AIML | III |
| CF_B25EA0302_... | Principles of Artificial Intelligence | AIDS, AIML | III |
| CF_B25EA0303_... | Portfolio Development | AIDS, AIML | III |
| CF_B25EA0304_... | Application Development-1: Web Design | AIDS, AIML | III |

> **AIML note:** The 4 AIDS+AIML shared courses (B25EA030x) are filed here because both programmes share the same course code. AIML-exclusive courses (if any) belong in `AIML/`.

### CSE/ — 8 files

| File | Course | Sem |
|---|---|---|
| CF_B25CS0303_... | Computer Organization and Architecture | III |
| CF_B25EF0301_... | Object Oriented Programming using Java | III |
| CF_B25EF0302_... | Portfolio Building | III |
| CF_B25EF0303_... | Application Development-1: Web Application Development | III |
| CF_B24CI0309_... | Introduction to Design Thinking | VIII |
| CF_B24CS0301_... | Professional Ethics | VIII |
| CF_B24EE0310_... | Universal Human Values | VIII |
| CF_B24ED0501_... | Indian Knowledge Systems | VIII |

### AIML/, CSIT/, ISE/, IoT/ — empty (no programme-exclusive coded courses in scheme docs yet)

Semesters IV–VIII for these programmes have not yet been assigned course codes in the 2026 scheme.
Add files here as those courses are designed.

---

## File naming

```
CF_<CourseCode>_<ShortCamelCaseTitle>.md
```

If no course code has been assigned yet (common in Sem IV–VIII):

```
CF_Sem<Roman>_<ShortCamelCaseTitle>.md
```

Update the filename once the official code is assigned.

---

## YAML front-matter (every course file)

Every file begins with a YAML block pre-filled from the scheme of instruction:

```yaml
---
course_code: "B25CS0301"
title: "Data Structures and Algorithms"
programs: [AIDS, AIML, CSE]
semester: III
category: HC
ltpc: "1-1-1-3"
contact_hours_per_week: 5
cie: 50
see: 50
total_marks: 100
aicte_category: PCC
level: "TBD — verify in Curriculum_Visual_Map.md"
status: skeleton        # → change to "designed" after course design, "verified" after checklist pass
---
```

---

## How to complete a skeleton file

1. Open the file in Claude Code — the **`reva-course-designer`** skill triggers automatically.
2. Confirm programme, L-T-P-C, and dual-level (A/Adv/A+Adv) from `Docs/<PROGRAM>-v1.md` and `Curriculum_Visual_Map.md`.
3. Fill in §1–§13 and §14 awareness/advanced split via the workflow (Path A or Path B).
4. After faculty review, run **`reva-course-reviewer`** to verify against the checklist.
5. Change `status:` in the front-matter from `skeleton` → `designed` → `verified`.
6. Commit and open a PR.
