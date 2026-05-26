Read every raw source file in the raw/ directory thoroughly. Extract the complete contents and create a structured knowledgebase wiki. Follow the conventions and structure defined in AGENTS.md.

## What to create

### 1. sources.md
Document every raw source file with:
- File path, type, description
- Metadata (title, author, publisher, date, ISBN, format, line count)
- Document structure (chapters, sections, major divisions)
- Any URLs or external references found in the source

### 2. overview.md
A high-level synthesis of the entire body of knowledge:
- What it is, who created it, why it matters
- Core thesis or central argument
- Key methodology or system (if one exists)
- Table of all major frameworks/concepts with brief descriptions and links
- How the pieces fit together
- Link to success stories or case studies

### 3. Entity pages (wiki/entities/)
Create a page for every person, company, product, or organization that plays a significant role. For each:
- H1 title is the entity name
- Bio/description: who/what they are
- Their role in the source material
- Key contributions, quotes, or attributes
- Cross-reference links to related entities and concepts
- Reference: "Source: `raw/[filename]`"

### 4. Concept pages (wiki/concepts/)
Create a page for every framework, method, model, rule, or standalone concept. For each:
- H1 title is the concept name
- Clear definition in the first paragraph
- Who created/developed it (if attributable)
- The framework itself: components, steps, letters of acronyms
- How to apply it, with examples from the source
- Tables where helpful (e.g., comparison tables, decision matrices)
- Cross-reference links to related concepts and step pages
- Reference: "Source: `raw/[filename]`"

Rule of thumb: if the source material introduces a named acronym, a multi-step process, a decision framework, or a mental model — it gets its own concept page.

### 5. Methodology/process step pages
If the source describes a step-by-step methodology, create a synthesis page that explains the overall system and a deep-dive page for each step. Each step page should cover:
- Where it fits in the overall methodology
- Core principles for that step
- Specific techniques, scripts, or frameworks used
- Common mistakes to avoid
- Real examples from the source
- Cross-reference links to related concept pages

### 6. Other synthesis pages as needed
Depending on the source material, create additional synthesis pages for:
- Common mistakes / pitfalls (if the source catalogs them)
- Success stories / case studies (if the source includes them)
- Any appendix-like content that warrants its own page
- Comparisons, FAQs, or "getting started" guides

### 7. index.md
Create a master catalog organized by category (Overview, Steps, Concepts, Entities, Sources). For each page:
- Relative markdown link
- One-line summary of what the page covers
- Keep categories consistent with the wiki structure

### 8. log.md
Create the log file with a first entry documenting the ingest:
- Date in YYYY-MM-DD format
- Type: "ingest"
- Description of what was created
- List of all pages created, grouped by category

## Quality requirements

### Page quality
- Every page starts with an H1 title
- Every page cites its source: "Source: `raw/[filename]`"
- Cross-reference other wiki pages using relative links: `[concept name](concepts/page.md)`
- Write in clear, scannable markdown — use tables, lists, and bold liberally
- Never include commentary, opinions, or content not found in the source
- Preserve the author's voice in direct quotes, but summarize in your own words

### Cross-references
- Every concept page should link to the step(s) where it's applied
- Every step page should link to the concepts it uses
- Entity pages should link to the concepts they created or are associated with
- Overview page should serve as a navigational hub

### Completeness
- No significant concept, framework, or entity from the source should be omitted
- Don't create pages for trivial mentions — only for things with enough substance to warrant their own page
- If a concept is only briefly mentioned, fold it into the most relevant parent page rather than creating a thin standalone page

## Lint pass (run after wiki creation)

1. Verify every cross-reference link resolves to an existing file
2. Verify every wiki page is listed in index.md
3. Verify log.md entries are in reverse chronological order
4. Fix any issues found
