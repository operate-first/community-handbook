# Style guide

## Overview

### Markdown

Documents are written in Markdown.
See the [Markdown Guide][2] for instructions on how to use this simple and versatile markup language.

### Naming

Documentation titles are pre-fixed by the type if applicaly (how-to or FAQ), while other significant documents simply have descriptive titles.
In titles, words are always separated by a hyphen.

#### Examples
* Significant documents: glossary, style-guide
* How-to guides: how-to-request-a-repository, how-to-use-o1-clone-tool

### Organization

There are two folders in the community handbook repository: content and contributing.
The content folder holds documentation related to task instructions and guides, while the contributing folder contains general information that is necessary for contributors to understand.
When adding to the handbook, place documentation in the applicable folder.
If you are unsure which folder to use, please ask for guidance in your issue or PR to the repository.


## Format

### Headings

Use `Title Case` when referring to the **Operate First Community Handbook**.
All other titles use `Sentence case`, meaning capitalization follows the same rules as that of a normal sentence (only the first word and proper nouns are capitalized).

### Line breaks

When writing paragraphs, start each sentence on a new line.
This format will render as a normal paragraph, but makes it significantly easier to edit a document.
Without this method, edits to one sentence of a paragraph will appear as a change to the entire paragraph on GitHub.
By starting each sentence on a new line, an edit to a sentence will show up as a change to only that sentence, making it easier to review and approve new modifications to a document.

#### An example

In Markdown:
>These two sentences are separated into two lines.<br>
This is our preferred method, as it makes it much easier to review changes to the paragraph.

Rendered:
>These two sentences are separated into two lines.
This is our preferred method, as it makes it much easier to review changes to the paragraph.

### Links

Use reference style links, as they are the easiest to read and do not clutter up the text.
They appear similar to footnotes in Markdown, but they render as hyperlinks.

#### An example

In Markdown:

>For instructions on reference style links, click \[here]\[1]<br>
...<br>
*At the bottom of the document:*<br>
\[1]: https://www.markdownguide.org/basic-syntax/#reference-style-links


Rendered:
> For instructions on reference style links, click [here][1]

The link in the example above is called an absolute path.
Absolute paths should only be used to link to a page outside of the community handbook repository.
When linking to another document within the repository, however, we prefer to use the relative path.

#### An example

Relative path:
>../content/how-to-request-a-repository.md<br>
In this case, the initial **..** is necessary because the style guide is located within the **contributing** folder of the community handbook repository.
Relative paths are relative to the location of the current file, so we need to move back one directory with the .. before we can specify the **content** folder and the document within it.<br>

Instead of:
>https://github.com/operate-first/community-handbook/blob/main/content/how-to-request-a-repository.md

### Templates

Our [template document][4] provides several templates for various document types: how-to, article, FAQ, and so forth.
To use the template document:
1. A writer picks one of the templates and discards the rest of the markup.
1. The templates are displayed as code blocks by indenting 4 characters; this makes the markup visible on the rendered page. To use the template, the 4 characters must be removed.


## Content

### Overview

The handbook strives to be as accurate and up-to-date as possible.
It is crucial that the documentation provides clear, detailed instructions that match the actual experience of someone attempting to follow those instructions.

### Terms and Language

We believe that consistency of language is extremely important to the growth of our initiative and the health of our community.
We want to ensure that the language surrounding Operate First as a whole is clear and accessible to everyone.
To aid in this effort, we have compiled a glossary of basic terms and definitions crucial to understanding Operate First.
Please refer to this [glossary][3] for explanations of these important terms.

[1]: https://www.markdownguide.org/basic-syntax/#reference-style-links
[2]: https://www.markdownguide.org/
[3]: https://github.com/operate-first/community/blob/main/glossary.md
[4]: template-handbook-article.md
