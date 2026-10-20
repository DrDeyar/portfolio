---
layout: post
title: "Phase 1 — Sprint 1–2 and Quiz Retrospective"
permalink: /csp/sprint-3/phase-1/retrospective/
categories: [CSP, Retrospective]
toc: true
---

## Assignment and evidence

The [Sprint 3 assignment chart](https://pages.opencodingsociety.com/csp/sprint-3/) assigns **1 point** to “Sprint 1-2,Quiz Retro,” due in **Phase 1**. This retrospective reviews portfolio evidence against the course's Sprint 1 onboarding/programming goals and Sprint 2 full-stack foundations. It does not redo the Beyond Perfunctory assignment.

**Quiz review:** **61/66 (92.4%)**. All five missed questions are documented below with the selected answer shown in the feedback, the correction, an explanation, and a new practice example.

## Sprint 1: tools, portfolio, and development workflow

My portfolio contains a personalized [About page]({{ '/about/' | relative_url }}) and a GitHub Pages/Jekyll structure. Its [revision history](https://github.com/DrDeyar/portfolio/commits/main/) records repeated changes to page layout, photo presentation, and styling. This is evidence of iteration on a working website rather than a single finished screenshot.

A useful lesson from this history is that the source, build, and rendered page must all be checked. A local file can look correct while a template engine or missing stylesheet prevents the website from building correctly.

### Concrete debugging evidence

| Evidence | What changed | Lesson to carry forward |
| --- | --- | --- |
| [Strings build fix, `0af49a7`](https://github.com/DrDeyar/portfolio/commit/0af49a730021cef019954efbe2b0010b4dffd8ea) | The homework's JSON-style f-string was rewritten to avoid adjacent opening braces in the notebook source. | In a Jekyll notebook workflow, Python text also passes through a template system. Check the rendered build as well as Python output. |
| [Button import fix, `fd7ea1d`](https://github.com/DrDeyar/portfolio/commit/fd7ea1d506b80fc8f53cfd05a395dc0a6b90b7c8) | A Sass import changed from `variant-runner` to `variant-dragdrop`. | Check imported filenames and dependencies when debugging styles, instead of assuming the page's HTML is the problem. |

These commits support specific observations about the work. They do not establish a quiz score or prove that every earlier task was completed.

## Sprint 2: programming and full-stack concepts

The existing notebooks provide examples for explaining programming concepts. Reviewing them here does not create or resubmit Phase 2 homework.

| Concept | Existing evidence | Explanation |
| --- | --- | --- |
| Sequencing and arithmetic | [Math expressions notebook](https://github.com/DrDeyar/portfolio/blob/main/_notebooks/homework/2026-09-30-3-03-math-expressions-hw.ipynb) | Weekly cost is calculated before monthly cost, and monthly cost before the total with an enrollment fee. Later steps depend on earlier results. |
| Strings and collections | [Strings notebook](https://github.com/DrDeyar/portfolio/blob/main/_notebooks/homework/2026-09-30-3-04-strings-hw.ipynb) | `strip()` removes outer whitespace and `split(",")` creates a list of fields. Indexing retrieves fields, while slicing retrieves part of a string. |
| Selection and parameters | [Conditionals notebook](https://github.com/DrDeyar/portfolio/blob/main/_notebooks/homework/2026-09-30-3-06-conditionals-hw.ipynb) | `score_message(message, amount_requested, known_contact)` uses three inputs to accumulate risk. Separate `if` statements can all contribute; the final `if/elif/else` chain chooses one advice message. |

### Full-stack explanation to practice

A frontend collects an input and sends an HTTP request. A Flask route validates that input, calls the relevant model or other logic, and returns data, commonly JSON. JavaScript reads the response and updates the page. For example, a search form can send a GET request containing a search term and display the returned records.

A database stores data, while a collection in an algorithm groups values for processing. Using a database alone does not demonstrate a student-developed procedure containing sequencing, selection, and iteration. Likewise, a successful login proves identity; authorization determines which actions that user may perform.

## Quiz retrospective — 61/66 (92.4%)

My score was **61 out of 66 (92.4%)**. The supplied AP Classroom feedback identifies five incorrect questions, each worth one point: **19, 39, 40, 50, and 64**. The corrections below use that feedback. The screenshots and private results link are not reproduced on this public page.

### Correction summary

| Question | Topic | Answer shown selected | Correct answer |
| --- | --- | --- | --- |
| 19 | E-book metadata | C — publication date | A — an archive containing earlier versions |
| 39 | Open Internet standards | C — permission to reuse Internet material | A — interoperability across manufacturers and developers |
| 40 | Exam-score data analysis | C — I and III only | D — I, II, and III |
| 50 | Searching a list | A — binary search only | B — linear search only |
| 64 | Cloud computing | A — eliminates routing redundancy | B and C — improved collaboration and new data-security concerns |

Question 64 requires two answers. The screenshot shows A marked incorrect and B/C marked correct; it does not establish another selected answer.

### Q19: descriptive metadata versus stored content

I selected the publication date as the information least likely to be metadata. **The correct choice is the archive of previous versions.** A publication date describes a book and can help users search or filter results, just as an author, title, and genre can. An archive containing earlier books is stored content, rather than a descriptive field about the current book. A version number or reference to an archive could be metadata; the archive itself is the distinction here.

**Correction to remember:** Metadata describes data. When the prompt asks for the least likely example, separate descriptive attributes from the underlying content.

**New practice example:** For a photograph, the date taken, dimensions, and camera model are metadata. A folder containing all earlier edited image files is content, not merely a descriptive attribute.

**SFI connection:** A specification number, category, and effective date describe a document. The PDF itself is the document content. That distinction helps define useful search fields.

### Q39: open standards versus copyright permission

I selected the statement about freely reusing Internet material for noncommercial purposes. **The correct answer is interoperability:** shared standards let hardware and software made by different organizations communicate.

“Open” describes the availability of a technical standard, not the copyright status of everything transmitted with it. Noncommercial use does not automatically grant permission to copy a work. Standards also do not eliminate latency or guarantee error-free software.

**Correction to remember:** A protocol defines how systems communicate. A license or other applicable legal permission determines how a work may be reused.

**New practice example:** A browser and a web server built by different companies can exchange requests and responses using HTTP. A copyrighted image returned by that server does not become freely reusable just because HTTP is an open standard.

**SFI connection:** Our frontend and Flask backend can communicate using a shared HTTP/JSON contract. That does not give the project unrestricted reuse rights over linked specification PDFs.

### Q40: deriving new measures from existing data

I selected I and III, omitting the average increase caused by the replacement policy. **All three measures can be determined**, so D is correct. The dataset includes each student's midterm score, final score, and adjusted total; the unadjusted total can therefore be reconstructed.

For midterm score `M` and final score `F`:

- Original total: `M + F`.
- Adjusted total: `max(M, F) + F`.
- Increase: adjusted total minus original total, equivalent to `max(F - M, 0)`.

Then:

1. **I:** Average the adjusted totals.
2. **II:** Calculate each student's increase and average those increases.
3. **III:** Count students with a positive increase and divide by the number of students.

**New practice example:**

| Student | Midterm | Final | Original total | Adjusted total | Increase |
| --- | --- | --- | --- | --- | --- |
| A | 60 | 85 | 145 | 170 | 25 |
| B | 90 | 80 | 170 | 170 | 0 |

The average adjusted total is **170**. The average increase across both students is **12.5**, and the proportion benefiting is **1/2 = 50%**. The denominator for the average increase is all students, not just those whose scores improved.

**Correction to remember:** Before deciding a measure cannot be determined, check whether it can be calculated from the available fields. A derived value does not need its own stored column.

### Q50: linear search versus binary search

I chose binary search. **The procedure is a linear search:** it visits each element and compares it with the target. It returns true immediately on a match; otherwise it returns false after the entire list has been examined. It works on an unsorted list.

Binary search compares against a middle element and repeatedly reduces the search range. For the usual numeric or alphabetic comparison, that requires the list to be sorted consistently. A loop containing a comparison is not enough to identify binary search.

**New practice example:** Searching `[12, 4, 9, 2]` for `9` compares `12`, then `4`, then `9`, and returns true after three comparisons. Searching for `20` examines all four elements and returns false. An empty list also returns false because the loop has no elements to visit.

**Correction to remember:** Trace which elements are inspected and how the search range changes. Linear search may inspect all `n` items; binary search repeatedly halves a sorted search range.

**SFI connection:** A proposed procedure that examines every specification record to decide whether it matches is a linear scan. Using a search box or a database does not by itself make the algorithm binary search.

### Q64: cloud benefits, security, and fault tolerance

My screenshot shows the incorrect selection that cloud computing eliminates the need for routing redundancy. **The correct pair is B and C:** cloud computing supports collaboration and introduces data-security concerns.

Cloud-hosted services let people access and edit shared information from different locations. They also require attention to access permissions, account security, and exposure of remotely stored data. Redundant network routes are still needed for fault tolerance when a connection or part of the network fails. Moving a file into the cloud does not remove intellectual-property obligations either.

**New practice example:** A team can edit a shared online planning document together. If its sharing settings accidentally make private information public, that is a data-security problem. If one network route fails, an alternative route can still be needed to reach the service.

**Correction to remember:** Cloud computing changes where resources are hosted and how they are shared; it does not remove the Internet's reliability needs or ownership rules.

## What the mistakes have in common

The corrections highlight distinctions I need to keep clear: metadata versus content, communication standards versus reuse permission, stored fields versus derived measures, linear scanning versus halving a search range, and cloud convenience versus fault tolerance. These are specific review targets supported by the feedback; the screenshots do not explain my private thought process at the time.

For future questions, I will underline words such as **LEAST**, evaluate each numbered statement separately, and check how many answers are required. I will trace search steps and write out calculations before eliminating an answer. These are planned habits, not a claim that I have already retaken the assessment.

## Improvement plan

1. Revisit the five correction examples above, then explain each distinction without looking at the answer. Use new values for the data-analysis and list-search examples to check understanding.
2. Before changing a website, record the expected result. After changing it, run the build and check the affected rendered page.
3. For a full-stack feature, trace one input through the frontend, request, backend handler, data operation, response, and displayed output.
4. Use normal, boundary, and invalid cases. Record expected and actual results instead of treating “the server started” as a complete test.
5. Keep the personal feature's purpose, collection, procedure, parameter, and call explicit. Review whether sequencing, selection, and iteration occur inside the same proposed procedure.

## Sources and preparation note

- [Sprint 3 requirements and point chart](https://pages.opencodingsociety.com/csp/sprint-3/)
- [Course sprint goals](https://github.com/open-coding-society/pages/blob/main/_projects/systems/courses/data/csp.yml)
- [Design Thinking guidance](https://pages.opencodingsociety.com/agile/design_thinking)

Prepared with AI assistance from the course source, existing portfolio files, and the five AP Classroom feedback screenshots supplied by Deyar. The corrections paraphrase the feedback and add original practice examples; they do not claim that a retake or independent practice session has occurred.
