# Curating Knowledge Collections -- Slide Deck Content

> CUNY AI Lab Sandbox Workshop
> Source: `index.html`
> Upstream: <https://github.com/CUNY-AI-Lab/knowledge-collections>

---

## Slide 1 -- Title (`title-slide`)

**Curating Knowledge Collections**
A Workshop for the CUNY AI Lab Sandbox
March 23, 2026

---

## Slide 2 -- Workshop Roadmap (`layout-full-dark`)

**Three Weeks, Three Skills**

| Date | Session | Description |
|------|---------|-------------|
| March 16 (Last Week) | Composing System Prompts &#10003; | Learned how system prompts can help orchestrate and constrain AI models to address specific course goals |
| March 23 (This Week) | Curating Knowledge Collections | Upload syllabi, readings, and relevant sources to ground AI models in course materials |
| March 30 | Customizing Skills & Tools | Build specialized skills, tools, and workflows tailored to your courses |

---

## Slide 3 -- Sign In and Navigate to Workspace (`layout-content`)

**Label:** Getting Started

Before we begin, make sure you can access the CUNY AI Lab Sandbox.

1. Go to chat.ailab.gc.cuny.edu and sign in with your CUNY account
2. Open **Workspace** (top left, three rows below "New Chat")

**Next:** Once you're signed in and can see the Workspace menu, you're ready to set up your model card on the next slide.

---

## Slide 4 -- Set Up Your Model Card (`layout-split`)

**Label:** Before We Start

Knowledge collections attach to a model card in Workspace > Models. After you build your collection, complete these steps to bring everything together.

1. **Go to Workspace > Models:** Click + New Model to create one, or open the model card you built last week
2. **Name the model card:** Give it a descriptive name tied to your course, for example ENGL 101 Writing Scaffold or History 202 Source Analysis Tool
3. **Select a base model:** Choose a model from the Sandbox (DeepSeek, Qwen3, Llama, etc.)
4. **Add your system prompt:** Scroll to System Prompt under Model Params. Paste the prompt you wrote last week.
5. **Save your work:** Click the Save button. Your model card is now ready for a knowledge collection.

**Keep this tab open.** You will return to this model card at the end of today's exercise to attach the knowledge collection you build.

**Stage:** Single image -- `slide4-c.png` (Workspace > Models landing page)

---

## Slide 5 -- Test Your Model in Chat (`layout-split`)

**Label:** Dry Run

Your model is saved. Now test it to make sure it responds as expected before attaching a knowledge collection.

1. Click **New Chat** in the top left
2. Click the **model selector** dropdown at the top of the chat
3. Choose your newly created model from the list
4. Send a test message related to your course and observe the response

**Look for:** Does your custom model respond as expected? How has your system prompt shaped its output?

**Stage:** Screenshot placeholder (testing a custom model in chat)

---

## Slide 6 -- What Is a Knowledge Collection? (`layout-split`)

**Label:** The Basics

A **knowledge collection** is a set of documents you upload to ground an AI model in specific course materials. The model retrieves relevant passages from these documents when responding to students.

> Think of it as the **reading list** for your AI tool: the sources it can reference, the assignments it knows about, and the disciplinary context it works within.

**Key distinction:** The *system prompt* tells the model how to behave. The *knowledge collection* tells it what to draw on. Together, they create a tool grounded in your teaching context.

*Next we'll show you where to find knowledge collections in the Sandbox and how to curate and use them with pedagogical intent.*

---

## Slide 7 -- Where to Find Knowledge Collections (`layout-split`)

**Label:** Open WebUI

Your model is open. Now you need two things to attach to it:

- **Step 1 (already done):** Your Model File is open in Workspace > Models. System prompt is set. This is where the collection will attach.
- **Step 2 (today):** Go to Workspace > Knowledge to create your collection. Upload PDFs and documents, then return to your model to attach it under Knowledge.

**Order matters:** Model first, collection second. The system prompt defines behavior; the knowledge collection defines the source documents the model queries. Both live in the same model file.

**Carousel:**
- `slide4-c.png` -- Your Model: Already Open
- `slide4-d.png` -- Where the Collection Attaches
- `slide4-a.png` -- Create Your Collection: Step 1
- `slide4-b.png` -- Create Your Collection: Step 2

---

## Slide 8 -- Why Knowledge Collections Matter (`layout-content`)

**Label:** Why Bother?

A student asks: **"What should I focus on for the midterm essay?"**

**Without Knowledge Collection** *(appears first)*
"For a midterm essay, you should generally focus on your thesis statement, use evidence from your readings, and structure your argument clearly. Make sure to address counterarguments."
*Generic advice. No connection to the assignment or the course readings.*

**With Knowledge Collection** *(revealed on next advance)*
"Based on the assignment prompt, your essay should analyze one primary source from the Reconstruction unit using the SOAPS framework we practiced. The prompt emphasizes evidence and sourcing. Which document are you considering?"
*Grounded in the actual assignment and course methodology.*

---

## Slide 9 -- What Can You Upload? (`layout-full-dark`)

**Label:** Building Materials

Uploaded files ground AI models in context and help shape their responses. These documents are stored on CUNY's self-hosted servers and made private by default.

| Document Type | Description |
|---------------|-------------|
| Syllabi | Course schedule, learning objectives, policies, and expectations |
| Assignment Prompts | Instructions, requirements, and criteria for each assignment |
| Rubrics | Grading criteria so the model can reference specific expectations |
| Course Readings | Primary sources, articles, chapters, and excerpts students are working with |
| Lecture Notes | Key concepts, frameworks, and terminology from your lectures |
| Style Guides | Citation formats, disciplinary conventions, writing guidelines |
| Sample Work | Exemplars that model the kinds of work you expect |
| Data Sets | Spreadsheets, CSV files, or structured data students analyze in labs or projects |
| Glossaries | Discipline-specific terminology, definitions, and key concepts for the course |
| Problem Sets | Exercises, practice questions, or worked examples with solutions |
| Lab Protocols | Step-by-step procedures, safety guidelines, and equipment instructions |
| Case Studies | Real-world scenarios, historical cases, or clinical examples used in coursework |

**A note on data and access:** When a student asks a question, only the most relevant passages from your collection are retrieved and injected into that single prompt as context. The model reads those passages in the moment and cannot store or reproduce them outside the conversation. Your source materials are referenced, not exposed.

---

## Slide 10 -- How the Model Uses Your Documents (`layout-split`)

**Label:** Retrieval-Augmented Generation

**Section label:** Under the Hood

When a student asks a question, the system doesn't feed the entire collection to the model. It searches for the most relevant passages and uses them as the basis for its response.

- **Chunking:** Your documents are split into smaller passages when uploaded
- **Search:** The student's question is matched against those passages
- **Injection:** Closest matches appended to model's context window
- **Response:** Model generates output grounded in retrieved passages

**Implication:** Short, focused documents with clear headings retrieve better than long, unstructured files. In other words, the way you organize your materials matters.

---

## Slide 11 -- What Makes a Good Knowledge Collection? (`layout-divider`)

**Section label:** Part I: Example 1
Starting with Composition & Writing

---

## Slide 12 -- Composition: The Bare Minimum (`layout-content`)

**Label:** Composition & Writing (progression: 1 of 3)

**Weak:** Collection contains only `syllabus.pdf` (14 pages)

**What goes wrong?**
- One large document retrieves poorly: retrieved passages are often irrelevant
- No assignment context for the revision task
- No readings or reference materials for the model to draw on

---

## Slide 13 -- Composition: Getting Warmer (`layout-content`)

**Label:** Composition & Writing (progression: 2 of 3)

**Getting There:** Collection contains syllabus.pdf, essay-1-prompt.pdf, mla-style-guide.pdf

**What improved?**
- Separate documents let the model find what it needs
- Assignment prompt gives the model context for the revision task
- Style guide helps with formatting questions

**What's still missing?**
- No course readings for the model to reference during analysis
- No common feedback patterns to guide revision
- No instructor notes on what substantive revision looks like in this course

---

## Slide 14 -- A Collection That Grounds Revision (`layout-content`)

**Label:** Composition & Writing (progression: 3 of 3)

**Strong collection with three layers:**

Course Framework: syllabus.pdf, revision-philosophy.txt
Assignment Materials (Essay 1: Rhetoric in Popular Media): essay-1-prompt.pdf, common-feedback.txt
Reference Materials: mla-style-guide.pdf, strong-intro-examples.txt, revision-checklist.pdf

---

## Slide 15 -- Primary Source Analysis (`layout-divider`)

**Section label:** Example 2

---

## Slide 16 -- History: The Bare Minimum (`layout-content`)

**Label:** History (progression: 1 of 3)

**Weak:** Collection contains only `textbook-chapter-12.pdf` (42 pages)

**What goes wrong?**
- A full textbook chapter is too long and too general: retrieved passages are often irrelevant
- No primary sources for the model to help students analyze
- No framework like SOAPS for the model to scaffold source analysis

---

## Slide 17 -- History: Getting Warmer (`layout-content`)

**Label:** History (progression: 2 of 3)

**Getting There:** Collection contains syllabus.pdf, source-analysis-assignment.pdf, primary-source-1.pdf (Freedmen's Bureau report, 1866), primary-source-2.pdf (Congressional testimony, 1871)

**What improved?**
- Includes actual primary sources students are working with
- Assignment prompt gives the model task-specific context
- Documents are separate and focused

**What's still missing?**
- No contextual background for the model to draw on when students ask about the period
- No SOAPS framework or equivalent to guide source analysis
- No source metadata (author, date, document type) to support sourcing questions

---

## Slide 18 -- A Collection That Fosters Historical Thinking (`layout-content`)

**Label:** History (progression: 3 of 3)

**Strong collection with three layers:**

Course Framework: syllabus.pdf, soaps-framework.txt
Primary Sources (Reconstruction Unit): freedmens-bureau-report-1866.pdf (with metadata), congressional-testimony-1871.pdf (with metadata), source-context-notes.txt
Reference Materials: period-timeline.txt, common-analysis-errors.txt, chicago-citation-guide.pdf

---

## Slide 19 -- Close Reading & Literary Analysis (`layout-divider`)

**Section label:** Example 3

---

## Slide 20 -- Literature: The Bare Minimum (`layout-content`)

**Label:** Literature & Cultural Studies (progression: 1 of 3)

**Weak:** Collection contains only `course-reader.pdf` (180 pages)

**What goes wrong?**
- A 180-page file retrieves unpredictably: the model might pull from the wrong text entirely
- No assignment context or close-reading framework
- No separation between literary texts and critical essays

---

## Slide 21 -- Literature: Getting Warmer (`layout-content`)

**Label:** Literature & Cultural Studies (progression: 2 of 3)

**Getting There:** Collection contains syllabus.pdf, close-reading-assignment.pdf, sonny-blues-baldwin.pdf, new-criticism-overview.pdf

**What improved?**
- Individual literary text rather than an omnibus reader
- Assignment prompt provides task-specific context
- Critical framework document gives the model methodological grounding

**What's still missing?**
- No annotated examples showing how to move from observation to interpretation
- No key terms for the current unit (e.g., tension, irony, ambiguity)
- No instructor notes on what close reading looks like in this course

---

## Slide 22 -- A Collection That Fosters Close Reading (`layout-content`)

**Label:** Literature & Cultural Studies (progression: 3 of 3)

**Strong collection with three layers:**

Course Framework: syllabus.pdf, new-criticism-framework.txt
Assignment Materials (Close Reading Essay): close-reading-assignment.pdf, annotated-passage-example.txt
Literary Texts (Current Unit): sonny-blues-baldwin.pdf, passage-selections.txt

---

## Slide 23 -- Curation Best Practices (`layout-grid`)

**Section label:** Part II

- **One Document, One Purpose:** Upload separate files; focused documents retrieve better than omnibus ones
- **Add Metadata and Headings:** Titles, authors, dates, and section headings serve as retrieval anchors
- **Supply What's Not in the Documents:** Include meta documents like "common-feedback.txt" that signpost how to use sources in the collection
- **Update Per Unit:** Swap course materials as the semester progresses; up-to-date collections outperform semester-wide ones

---

## Slide 24 -- Common Pitfalls (`layout-content`)

**Label:** Watch Out

- **Dumping Everything In:** Uploading every reading dilutes retrieval; start small and add materials as you test
- **One Giant PDF:** A 200-page course reader retrieves unpredictably; short, well-labeled documents work far better
- **Forgetting the System Prompt:** Without explicit instructions for drawing on the collection, it is just a pile of documents
- **Assuming Full Coverage:** Only retrieved passages appear in each response; if something is critical, give it its own file

---

## Slide 25 -- Build Your Collection (`layout-content`)

**Section label:** Part III: Hands-On
**Label:** Exercise

Pick one assignment from your course. You will build a knowledge collection for it, one layer at a time.

1. **Course Context:** Syllabus sections, weekly schedule
2. **Assignment Materials:** Instructions, feedback examples
3. **Source Materials:** Excerpted readings, primary sources

---

## Slide 26 -- Layer 1: Course Framework (`layout-split`)

**Label:** Step 1

These documents give the model a picture of your course: its goals, structure, and the methods students are expected to use.

- What are the course's learning objectives?
- What analytical framework or methodology is central to the course?
- What course-level context would help the model support those goals?

**Template (copyable):**
```
Recommended uploads:

1. syllabus.pdf
   - Course schedule, objectives, and policies

2. [framework-name].txt
   - The analytical method students use
   - Write it out in plain language with definitions
```

**Your turn:** What framework or methodology is central to your course? Write a short document (1-2 pages) explaining it in the terms you use with students.

---

## Slide 27 -- Layer 2: Assignment Materials (`layout-split`)

**Label:** Step 2

These documents define the current task and help the model align its responses with your specific learning objectives.

- What does the assignment ask students to do?
- What does strong work on this assignment look like?
- What patterns come up most often in your feedback?

**Template (copyable):**
```
Recommended uploads:

1. [assignment]-prompt.pdf
   - The assignment instructions

2. common-feedback.txt
   - 5-10 patterns you see every semester

3. strong-examples.txt (optional)
   - Excerpts showing what strong work looks like
```

**Your turn:** Which assignment stands to benefit? Try curating assignment instructions alongside a shortlist of common feedback patterns for starters.

---

## Slide 28 -- Layer 3: Source Materials (`layout-split`)

**Label:** Step 3

Upload the readings and reference materials students are working with in the current unit. This grounds the model in the actual texts.

- What texts are students reading for this assignment?
- Are there reference documents (timelines, glossaries, citation guides)?
- Can you add brief metadata or context for each source?

**Template (copyable):**
```
Recommended uploads:

1. [reading-title].pdf
   - Individual files per text (not one big reader)
   - Add a header with: title, author, date, source

2. context-notes.txt (optional)
   - 2-3 sentences of context per source

3. [reference-guide].pdf
   - Citation style guide, glossary, or timeline
```

**Your turn:** Upload 1-3 readings for your chosen assignment. If they're in a single PDF reader, split them into separate files first.

---

## Slide 29 -- Prompt + Collection (`layout-split`)

**Label:** Putting It Together

Your system prompt and knowledge collection work together. The prompt defines *behavior*. The collection provides *context*.

**System Prompt:**
"You are a writing revision scaffold for ENGL 101. When a student shares a draft, ask them to identify which area they want to work on first. Reference the assignment prompt and common-feedback documents before responding."

**Knowledge Collection:**
syllabus.pdf, revision-philosophy.txt, essay-1-prompt.pdf, common-feedback.txt, mla-style-guide.pdf, strong-intro-examples.txt

**Test it:** Ask the model a question only answerable from your collection. If it gives generic advice, the retrieval isn't working. Check your document structure.

---

## Slide 30 -- The Road Ahead (`layout-full-dark closing-slide`)

**Label:** Coming Up

| Date | Session | Description |
|------|---------|-------------|
| March 16 | System Prompts &#10003; | Configured how the model responds and scaffolds learning |
| March 23 (Today) | Knowledge Collections &#10003; | Grounded the model in your course materials so it can reference real documents |
| March 30 (Next Week) | Skills & Tools | Build specialized skills, tools, and workflows tailored to your courses |

Each workshop builds on the last. The system prompt you wrote last week now drives a model grounded in the knowledge collection you built today. Next week, you'll extend it with custom skills and tools.

ailab.gc.cuny.edu

---

_Last synced: 2026-03-22. Upstream: CUNY-AI-Lab/knowledge-collections @ main. Update both files together._

## Changelog

### 2026-03-22
- Full SLIDES.md rewrite to sync with index.html (30 slides)
- Heading format standardized: `## Slide N -- Title (\`layout-class\`)`
- Added slides 3-5 (model setup workflow from commit 6cd0370)
- Added upstream URL to header blockquote
- Replaced em dashes in rendered content with colons
- Added data-privacy note to slide 9 (What Can You Upload?)
- Added sync timestamp and changelog section
- Section dividers previously listed separately (old slides 9, 11, 12, 16, 20, 24, 29) are now folded into adjacent content slides; this file reflects the merged HTML structure
