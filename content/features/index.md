---
title: "How it works"
aliases: ["/architecture/"]
---
{{< section id="intro" >}}
<div class="page__head">

# How it works

</div>
<div class="prose">

**Exeges tracks and versions every source you rely on, records every conclusion your team reaches along with supporting evidence, and keeps a replayable history of every decision and the reasoning behind it, including disagreements.**  

Evaluate a position with AI assistance. Ask a question in plain language and get an answer drawn from the whole set of documents and data. Turn agents loose on a section and let them investigate and offer analysis.

Put supporting material and associated positions on the record. Automatically monitor for change in anything your positions depend on, and review AI generated impact analysis.

Keep a durable, auditable, portable record of everything - in regular files that can be stored anywhere.

</div>
{{< /section >}}

{{< section id="mechanism" >}}
<div class="walk">

<div class="walk__step" id="the-grid">
<div class="prose">
<span class="eyebrow">Pull in information</span>

### Any source is versioned and citable

Documents, web pages, spreadsheets, video, and feeds from any API, public or private, are ingested as versioned sources with their structure intact.

A grid is then applied: every passage, every table cell, every second of a transcript is given a fixed address, the way latitude and longitude anchor a point on a map. 

We wrote about the design [here](/posts/the-grid/).

</div>
{{< plate name="grid" num="Image 1" alt="Five kinds of source on the left, a PDF, a web page, a spreadsheet, a video frame at a timecode, and an API request returning filings, converge on a grid mark and continue to one source on the right, version 3, with two earlier versions kept behind it. Every passage, cell and heading carries a small spot, and three carry address chips: section 2 paragraph 1, table 1 row 3 column 3, and the transcript at twelve minutes four seconds." >}}
Five kinds of source converge on one gridded, versioned source. On the right, version 3 of a filing with two earlier versions kept behind it. Three addresses are called out: section 2, paragraph 1; table 1, row 3, column 3; and a transcript at 12:04. Any line in the plates that follow ends on a spot like these.
{{< /plate >}}
</div>

<div class="walk__step" id="findings-on-the-grid">
<div class="prose">
<span class="eyebrow">Mapping Citations</span>

### References point to the grid

References can cite any point within a document or data. These can refer to anything: a person, a number, a summary, an image. They can also connect a process to source material: a review due by a date, or a position with its reasons. A finding can cite another finding, so the reasoning behind a position is on the record and searchable.

</div>
{{< plate name="references" num="Image 2" alt="A document, version 3 filed 2 March 2026, with six numbered findings around it, each joined by a fine line to one exact spot on the page: an entity, a review due by a date, an amendment, a position, a measure of 4.2 million dollars, and a summary." >}}
Six findings on version 3. Numbers 1, 3, 5, and 6 were produced by the platform; 2 and 4 were placed by a reader, and 4 cites 3. Each line ends on the one spot that supports the finding.
{{< /plate >}}
</div>

<div class="walk__step" id="the-gate">
<div class="prose">
<span class="eyebrow">Automatic verification</span>

### Nothing enters unverified

Before a reference is written, the text it cites is automatically checked. If the text is there, the reference attaches, verified at that version. If it is not, the write is refused. This avoids both hallucinations and mistakes: an agent cannot cite text that isn't there, and neither can a person.

How the check works: [The Verification Gate](/posts/the-verification-gate/).

</div>
{{< plate name="gate" num="Image 3" alt="Version 3 of a document on the left. On the right, a measure finding citing the text 4.2 in row 3 is joined to the table cell and stamped verified at version 3. A second finding citing 4.8 in the same row is pushed back and stamped refused, text not found at version 3." >}}
Two findings approach the same cell. The first cites “4.2”, which is on the page at version 3, and attaches as verified. The second cites “4.8”, which is not, and the write is refused.
{{< /plate >}}
</div>

<div class="walk__step" id="a-new-version">
<div class="prose">
<span class="eyebrow">Monitoring change</span>

### A new version arrives

New versions are aligned to the last one section by section, and every difference is recorded. Continuity survives renumbering and restructuring. Change is evidence like any other: anchored, queryable, replayable.

Every reference anchored to an old version is checked against the new one. Changes cause the reference to be updated as in doubt. No finding is ever moved to new text; a position stays on record until a person changes it. 

</div>
{{< plate name="version" num="Plate 4" alt="The same document, now version 4 filed 9 June 2026. Three findings are re-checked: the entity finding is badged still holds, the measure finding is badged in doubt because the cell it points to now reads 4.6 million dollars restated, and the summary finding is badged not yet checked. No finding has been moved." >}}
Version 4 replaces version 3, and every finding is checked against it. Finding 1 still holds. Finding 5 is in doubt: the cell it points to now reads $4.6M, restated, and the finding stays where it was. Finding 6 is not yet checked.
{{< /plate >}}
</div>

<div class="walk__step" id="the-record-compounds">
<div class="prose">
<span class="eyebrow">Compounding records</span>

### The record compounds

Creating a reference is something the system can react to: raise the section for the analyst who owns it, or put the next AI investigation to work. References help the next reader, human or agent, starts from what has already been established.

Agents work the corpus through a set of MCP tools: survey it, read a document, search it, inspect a diff, list the findings on a section, file one. They read their own coverage too: what has been examined, what was skimmed, what remains untouched, so a session builds on prior work.

</div>
{{< plate name="second-reader" num="Image 5" alt="On the left, six findings left by a first session in March 2026, each joined by a faint line to its spot on the page. A second session arrives in June, follows the third finding to its spot, and adds a seventh, a position that cites the third. Two gauges below read: findings inherited, six of six; pages re-read, none of four hundred and twelve." >}}
A second session arrives in June and starts from the six findings the first left in March. It reads them, visits one spot, and adds a seventh that cites the third. Nothing was re-derived, and no page was read twice.
{{< /plate >}}
</div>

</div>
{{< /section >}}

{{< section id="demo" band="true" >}}
{{< cta >}}
Demos are running now. [Get in touch](mailto:info@exeges.ai?subject=Exeges%20demo) to see one, or read what teams use it for: [use cases](/use-cases/).
{{< /cta >}}
{{< /section >}}
