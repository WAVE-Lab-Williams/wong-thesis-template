# About the theme
A minimal, mostly hard-coded, but hopefully well-organized template for the fulfillment of Yale dissertation requirements. Document settings are located in the `theming` directory. Build entrypoint is `main.tex`.

This template was built for a Dept. of Psychology dissertation, so citations are currently set to APA style and many conveniences required for a more math-heavy document are missing (symbol glossary, math environment layout settings, etc.)

This template shamelessly steals from the much fancier template

## Build

Compiled on Overleaf with pdfLaTeX, TexLive 2024

## Custom Commands and Environments

### Kaobox
A flexible box environment adapted from the kaobook theme.

**Usage:**
```latex
\begin{kaobox}[frametitle=Title of the box]
    Your text here
\end{kaobox}
```

**Parameters:**
- `frametitle`: Optional title for the box

### \fancyChapter
A command for creating enhanced chapter headers with optional subheaders and custom table of contents entries.

**Basic Usage:**
```latex
% Basic chapter with automatic numbering
\fancyChapter{Introduction}

% Chapter with subheader
\fancyChapter{Methods}[Experimental Procedures]

% Chapter with subheader and custom TOC entry
\fancyChapter{Results}[Statistical Analysis][Results and Discussion]
```

**Parameters:**
1. Main chapter title (required)
2. Subheader (optional)
3. Custom TOC entry (optional)

**Note:** Contains hardcoded layout values - use with caution and test in your specific context.

### \legendbox
Creates a colored square box matching the current font height.

**Usage:**
```latex
\legendbox{263238}  % Creates a box with color #263238
```

### \prettyurl
Formats URLs in a consistent, readable style. Note that we avoid changing
url fonts in the bibliography for fear of the thesis font police

**Usage:**
```latex
\prettyurl{https://example.com}
```

**Features:**
- Uses small typewriter font
- Maintains consistent URL styling

### \comment
Provides inline commenting functionality in blue color.

**Usage:**
```latex
Some text \comment{This is a comment} more text
```

**Features:**
- Comments appear in blue
- Properly handles line breaks

# Yale Dissertation Requirements

At time of writing, the [Yale dissertation formatting guidelines][registrar link] are as follows:

## Physical Requirements

- **Double spaced**
  - Exceptions: block quotations, bibliographic references, captions, footnotes should be single spaced, with a double space between each entry
- **Saved as a PDF** to be uploaded on the Degree Petition and Dissertation Submission page in DPRS
- **No paper copy** needs to be submitted
- **Margins**: Left side margin of 1.5”, 1” margin on all other sides

## Page Numbers

- 0.5” from any edge
- Preliminary pages are numbered with lower-case roman numerals, except title page and copyright page which are not numbered. The page following the copyright will be numbered (iii) and additional pages will be numbered sequentially
- The dissertation proper begins with page Arabic number “1” and runs consecutively to the end

## Font Size

- 10- to 12-point font
- Same font type should be used throughout, including header, footnotes, page numbers

## Order of Sections

1. Abstract
2. Title Page
3. Copyright Page
4. Table of Contents
5. Front Matter (acknowledgments, list of illustrations or tables, etc.)
6. Body of Text
7. Back Matter (appendices, bibliography, supplemental figures and tables, etc.)

## Abstract

- Placed immediately preceding the title page
- Heading centered on page
- Dissertation title and name of author must match title page
- Text of abstract below the heading, double spaced

**Example:**

```
Abstract

Full title of dissertation

Full name of author

Year of PhD conferral (e.g., 20XX)
```

## Title Page

- All text centered
- Month and year of conferral (e.g., May or June 20XX, or December 20XX)
- See attached example at end of guide

## Copyright Notice

- Typed 3” below top margin
- Format includes copyright symbol ©

**Example:**

```
© 20__ by [Student’s Name]

All rights reserved.
```

- Note: the copyright available through ProQuest is optional and an additional fee

## Tables and Figures

- Tables placed as close as possible to their reference in the text
- Heading at top of table
- Consecutive numbering throughout, or by chapter (e.g., 1.1, 1.2, 2.1, 2.2)
- Captions placed at bottom

## Sample Title Page

```
Dissertation Title: Subtitle

(first letter of each word in title should be capitalized)

A Dissertation

Presented to the Faculty of the Graduate School

of

Yale University

In Candidacy for the Degree of

Doctor of Philosophy

by

[Full Name of Author]

Dissertation Director: [Full Name of the Advisor(s)]

(or chairperson of advisory committee)

Month Year

(month of graduation, not of submission)
```

<!-- HYPERLINKS -->
[registrar-link]: https://registrar.yale.edu/students/dissertation-submission
[kaobook-link]: https://github.com/fmarotta/kaobook