I want you to plan a comprehensive system for writing essays in specified topic (currently analytic philoosophy).

The essay topic is usually an exam question (or a set of similar question from previous exams).

There are multiple levels of if and how a proposed/required outline for the output is given or not. 
- Often there is some general outline, 
- Sometimes the outline is quite specific. 
- Or there is a meta-outline saying how such essays are usually written (this is very similar to what is specified in tje icp.json file). 
- Sometimes ther is only a question (this is when I don't push for some specific argumentative direction).
- Sometimes onyl some general philosophical direction is given ("argue in terms of Horwich's Truth Minimalism).

The key process for you to research and plan is, that I want to specify sources in some parts of the outline. These cases might look like:

- Short exam question, and "argue for scientific realism as in Michael Huemers's book Understanding Knowledge, chapter 14 Scienctific Knowledge" <- you need this chapter
- Detailed outline and one or many bulletpoints must be taken from some specific article (Objection: counter example about zebra and mule, Huemer Understanding Knowledge chapter 2.3.4) <- you need this subchapter

Etc.

I can provide and organize sources in Markdown, PDF, TXT, HTML. Usually one chapter per file, but this might change, see below. I can convert some PDFs to MD, but PDFs are easier get to.

Markdown can have frontmatter metadata and they include table of content of that chapter, but not detailed index or some description for fulltext. 

It might be possible to split per-chapter Markdown to subchapters.

It might be possible to create some "index" of what is whare (suggest how).

There are books that span whole course, so various chapters and subchapters should probably be anotated somewhere so we dont put the whole book into context.

This project's set of SKILLs, CLAUDE.md, voice-dna.json and icp.json shoud create such a structure, that if I give you a well-formed short markdown with exam question (question itself, outline, some gerenal directions, general sources and per-bulletpoint sources) you should produce the whole essay.

Some notes: 
- Current state of project reflects boilerplate. Already personalized files are @context/voice-dna.json and @context/icp.json
@docs/ are boilerplate things, @knowledge/notes/writing-samples are what @voice-dna.json was created from, you probably won't need that except for reading how typical source is organized and what header it has.
- Is it possibe to have the index in human writable file? Like YAML.
- Sometimes I would like to add my comments to sources, like "Use this chapter whenever essay asks about scientific realism"
Investigate how to set it up includin the sources directory and indexes and processes how to create the indexes.

Also, my school structured like: Course > Module > Topic. Usually what I am focusing on is Module, because I have to pick a module for exam (each module has one module quesiton). So a question naturally arises if and how should we structure the sources. Maybe one idea might be to use symlinks. Is that feasible? Or can the current project somehow pick sources from specific directory? I would usually need at least course-level sources.

- Is it possibe to have the index in human writable file? Like YAML.
- Sometimes I would like to add my comments to sources, like "Use this chapter whenever essay asks about scientific realism"

That Understanding Knowledge book is a textbook for course Epistemology. However, various modules reference various chapters, or even subchapters. Module Memory in the course is basically exactly covered by chapter 11 so I can directly put chapter11.md as a (one) source. However in module Knowledge i want to pinpoint a specific subchapter (like # 2.3.4 Tracking account of knowledge). It would be nice if our system could somehow extract the chapter 2.3.4. Is that possible? Theoretically I can do some preprocessing, but it surely adds some overhead. However overhead is a price probably fine to pay when I get better results from LLMs.

A good part with the small index files woudl be that it decouples sources that come from OCR with my metadata. Sources can be regenerated (as if I spot a OCR mistake), though chapter names and numbers stay the same. 

My index files should be able to be generated initially from the OCRed soures (like copying TOC etc) and I should be able to add my notes to such toc ("when asked about sketpicism take this chapter"). When writing an essay, the resolving would work in reverse order: it would look at my index(es) and resolve the actual OCRed markdown/pdf sources and relevant line ranges. 