# Curating Knowledge Collections - Slide Deck Content

> CUNY AI Lab Sandbox Workshop
> Source: `index.html`

---

## Slide 1 - Title

**Curating Knowledge Collections**
A Workshop for the CUNY AI Lab Sandbox
March 23, 2026

---

## Slide 2 - Workshop Roadmap

**Three Weeks, Three Skills**

| Date | Session | Description |
|------|---------|-------------|
| March 16 - Last Week | Composing System Prompts ✓ | Learned how system prompts can help orchestrate and constrain AI models to address specific course goals |
| March 23 - This Week | Curating Knowledge Collections | Upload syllabi, readings, and relevant sources to ground AI models in course materials |
| March 30 | Customizing Skills & Tools | Build specialized skills, tools, and workflows tailored to your courses |

---

## Slide 3 - What Is a Knowledge Collection?

**The Basics**

A **knowledge collection** is a set of documents you upload to ground an AI model in specific course materials. The model draws on these documents when responding to students.

> Think of it as the **reading list** for your AI tool: the sources it can reference, the assignments it knows about, and the disciplinary context it works within.

**Key distinction:** The *system prompt* tells the model how to behave. The *knowledge collection* tells it what to draw on. Together, they create a tool grounded in your teaching context.

---

## Slide 4 - Where It Lives (Open WebUI)

In the CUNY AI Lab Sandbox, knowledge collections live in two places:

1. **Knowledge Base** - Go to Workspace → Knowledge to create a new collection. Upload PDFs, text files, and documents. Give it a name and description.
2. **Model Configuration** - Go to Workspace → Models, open your custom model, and attach your knowledge collection under Knowledge.

**Workflow:** Create the collection first, then attach it to your model. The system prompt you wrote last week tells the model *how* to use these materials.

---

## Slide 5 - Why Knowledge Collections Matter

A student asks: **"What should I focus on for the midterm essay?"**

**Without Knowledge Collection** *(appears first)*
"For a midterm essay, you should generally focus on your thesis statement, use evidence from your readings, and structure your argument clearly. Make sure to address counterarguments."
*Generic advice. No awareness of the assignment, the rubric, or the course readings.*

**With Knowledge Collection** *(revealed on next advance)*
"Based on the assignment prompt, your essay should analyze one primary source from the Reconstruction unit using the SOAPS framework we practiced. The rubric weights evidence and sourcing at 40%. Which document are you considering?"
*Grounded in the actual assignment, rubric, and course methodology.*

---

## Slide 6 - What Can You Upload?

Any document that helps the AI understand your course context. The model retrieves relevant passages when students ask questions.

| Document Type | Description |
|---------------|-------------|
| Syllabi | Course schedule, learning objectives, policies, and expectations |
| Assignment Prompts | Instructions, requirements, and criteria for each assignment |
| Rubrics | Grading criteria so the model can reference specific expectations |
| Course Readings | Primary sources, articles, chapters, and excerpts students are working with |
| Lecture Notes | Key concepts, frameworks, and terminology from your lectures |
| Style Guides | Citation formats, disciplinary conventions, writing guidelines |
| Sample Work | Anonymized exemplars that model the quality you expect |

---

## Slide 7 - Section Divider

**Under the Hood: How Retrieval Works**

---

## Slide 8 - How the Model Uses Your Documents

**Retrieval-Augmented Generation**

When a student asks a question, the system doesn't feed the entire collection to the model. It searches for the most relevant passages and includes them alongside the conversation.

- **Chunking:** Your documents are split into smaller passages when uploaded
- **Search:** The student's question is matched against those passages
- **Injection:** The top matches are included in the model's context window
- **Response:** The model generates an answer grounded in those passages

**Implication:** Short, focused documents with clear headings retrieve better than long, unstructured files. How you organize your materials matters.

---

## Slide 9 - Section Divider

**Part I: What Makes a Good Knowledge Collection?**

---

## Slide 10 - Section Divider

**Example 1: Composition & Writing**

---

## Slide 11 - Composition: The Bare Minimum

**Weak:** Collection contains only `syllabus.pdf` (14 pages)

**What goes wrong?**
- One large document retrieves poorly: the model pulls random passages instead of relevant ones
- No assignment-specific materials for the model to reference
- No rubric, no readings, no examples of what good work looks like

---

## Slide 12 - Composition: Getting Warmer

**Getting There:** Collection contains syllabus.pdf, essay-1-prompt.pdf, essay-1-rubric.pdf, mla-style-guide.pdf

**What improved?**
- Separate documents for different purposes: the model can find the rubric when asked about grading
- Assignment-specific prompt gives the model context for that unit
- Style guide helps with formatting questions

**What's still missing?**
- No course readings for the model to reference during analysis
- No examples of strong student work to model expectations
- No instructor notes on common student challenges

---

## Slide 13 - Composition: A Collection That Grounds Revision

**Strong collection with three layers:**

Course Framework: syllabus.pdf, revision-philosophy.txt
Assignment Materials: essay-1-prompt.pdf, essay-1-rubric.pdf, common-feedback.txt
Reference Materials: mla-style-guide.pdf, strong-intro-examples.txt, revision-checklist.pdf

---

## Slide 14 - Section Divider

**Example 2: Primary Source Analysis**

---

## Slide 15 - History: The Bare Minimum

**Weak:** Collection contains only `textbook-chapter-12.pdf` (42 pages)

**What goes wrong?**
- A full textbook chapter is too long and too general: retrieved passages are often irrelevant
- No primary sources for the model to help students analyze
- No methodological framework for the model to follow

---

## Slide 16 - History: Getting Warmer

**Getting There:** Collection contains syllabus.pdf, source-analysis-assignment.pdf, primary-source-1.pdf, primary-source-2.pdf

**What improved?**
- Includes actual primary sources students are working with
- Assignment prompt gives the model task-specific context
- Documents are separate and focused

**What's still missing?**
- No contextual background for the model to draw on when students ask about the period
- No rubric or analysis framework to guide the model's scaffolding
- No source metadata (author, date, document type) to support sourcing questions

---

## Slide 17 - History: A Collection That Fosters Historical Thinking

**Strong collection with three layers:**

Course Framework: syllabus.pdf, soaps-framework.txt, source-analysis-rubric.pdf
Primary Sources: freedmens-bureau-report-1866.pdf (with metadata), congressional-testimony-1871.pdf (with metadata), source-context-notes.txt
Reference Materials: period-timeline.txt, common-analysis-errors.txt, chicago-citation-guide.pdf

---

## Slide 18 - Section Divider

**Example 3: Close Reading & Literary Analysis**

---

## Slide 19 - Literature: The Bare Minimum

**Weak:** Collection contains only `course-reader.pdf` (180 pages)

**What goes wrong?**
- A 180-page file retrieves unpredictably: the model might pull from the wrong text entirely
- No assignment context or analytical framework
- No separation between literary texts and critical essays

---

## Slide 20 - Literature: Getting Warmer

**Getting There:** Collection contains syllabus.pdf, close-reading-assignment.pdf, sonny-blues-baldwin.pdf, new-criticism-overview.pdf

**What improved?**
- Individual literary text rather than an omnibus reader
- Assignment prompt provides task-specific context
- Critical framework document gives the model methodological grounding

**What's still missing?**
- No rubric for the model to reference when guiding analysis
- No examples of close-reading annotations or model analyses
- No glossary of literary terms the course uses

---

## Slide 21 - Literature: A Collection That Fosters Close Reading

**Strong collection with three layers:**

Course Framework: syllabus.pdf, new-criticism-framework.txt, literary-terms-glossary.txt
Assignment Materials: close-reading-assignment.pdf, close-reading-rubric.pdf, annotated-passage-example.txt
Literary Texts: sonny-blues-baldwin.pdf, passage-selections.txt

---

## Slide 22 - Section Divider

**Part II: Building Your Collection**

---

## Slide 23 - Anatomy of a Knowledge Collection

Every effective collection has three layers:

1. **Course Framework** — Syllabus, learning objectives, and the analytical framework students use
2. **Assignment Materials** — Prompts, rubrics, examples, and common feedback patterns
3. **Source Materials** — Readings, primary sources, and reference documents for the current unit

---

## Slide 24 - Layer 1: Course Framework

Start with the documents that establish your course's identity.

**Template:**
- syllabus.pdf (under 10 pages if possible)
- [framework-name].txt — the analytical method students use

**Your turn:** What framework or methodology is central to your course? Write a short document explaining it.

---

## Slide 25 - Layer 2: Assignment Materials

Upload the documents that define the current task.

**Template:**
- [assignment]-prompt.pdf
- [assignment]-rubric.pdf
- common-feedback.txt (5-10 patterns)
- strong-examples.txt (optional)

**Your turn:** Pick one assignment. Upload the prompt and rubric. Write a list of common feedback.

---

## Slide 26 - Layer 3: Source Materials

Upload the readings and reference materials for the current unit.

**Template:**
- [reading-title].pdf (individual files per text)
- context-notes.txt (2-3 sentences per source)
- [reference-guide].pdf

**Your turn:** Upload 1-3 readings. If they're in a single PDF reader, split them first.

---

## Slide 27 - Section Divider

**Part III: Best Practices & Pitfalls**

---

## Slide 28 - Curation Best Practices

- **One Document, One Purpose** — The model retrieves better from focused documents
- **Add Metadata and Headings** — Titles, authors, dates act as retrieval anchors
- **Write What the Model Can't Infer** — Instructor notes are more valuable than another PDF
- **Update Per Unit** — Swap materials as the semester progresses

---

## Slide 29 - Common Pitfalls

- **Dumping Everything In** — More documents means more noise
- **One Giant PDF** — Split into individual texts
- **Forgetting the System Prompt** — A collection without a prompt is a pile of documents
- **Assuming the Model Read Everything** — It only sees retrieved passages

---

## Slide 30 - Prompt + Collection

Your system prompt and knowledge collection work together. The prompt defines behavior. The collection provides context.

**Test it:** Ask the model a question only answerable from your collection. If it gives generic advice, check your document structure.

---

## Slide 31 - The Road Ahead

| Date | Session | Description |
|------|---------|-------------|
| March 16 | System Prompts ✓ | Defining how the AI thinks and teaches |
| March 23 - Today | Knowledge Collections ✓ | Grounding the AI in your course materials |
| March 30 - Next Week | Skills & Tools | Build custom skills, tools, and workflows tailored to your courses |

---

## Slide 32 - Closing

**Let's Build One Together**
Open the CUNY AI Lab Sandbox and curate a knowledge collection for your course

1. Pick one assignment from your course
2. Create a knowledge collection with 3-5 documents
3. Attach it to a custom model with your system prompt
4. Test it with a real student question

ailab.gc.cuny.edu
