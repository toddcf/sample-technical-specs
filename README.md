# Technical Writing

The following is my approach to writing documentation / technical specs.

These principles are also demonstrated in this set of [Sample Technical Specs](sample-technical-specs/global.md) I wrote.

## Principles

The following is generally based on writing specs in Confluence, but the same principles are valuable in general.

- Keep everything D.R.Y. (Don't Repeat Yourself). Each piece of information should be stated only once.
  - This typically means abstracting all common information up to a parent document, then hyperlinking each child document up to the parent.
    - Only hyperlink documents one level up. (If there are no specifics to add in a middle layer, simply pass the reader up to the next layer.)
  - This is important for keeping the specs easy to maintain. If a change must be made later, it will only have to be made in one place.
- Context first.
  - Place the following at the top of each document so readers can tell at a glance what is being described:
    - Title
    - Pathname *(if documenting a website)*
    - Screenshot *(large enough not to zoom, small enough not to scroll)*
- Keep all text super-lean.
  - Readers are less likely to skim or misinterpret.
  - Bullet points and sentence fragments are good.
- Write for clarity.
  - If a reader asks a question about the spec, something wasn't clear. Respond to the person, but then fix the spec.
- Use chronological, then alphabetical order.
  - If the specs describe something that occurs in a specific order (such as the steps of a purchase funnel), start each document title with a number so that the reader sees them in the order the user will navigate them.
  - Otherwise, fall back on alphabetical order.
- When describing an object (JavaScript, etc.), use bullet points for each property.
  - For visual clarity, indent all bullet points that represent a nested property.
  - Use the minimum amount of nesting required.
- Be wary of copying and pasting (especially in Confluence).
  - Confluence tends to obliterate formatting when pasting. (Sometimes it even looks correct until you save.)
  - When you copy/paste/edit, it is very easy to forget to change one detail. Then readers will either come to you with questions, or work off inaccurate specs.
  - Manually typing all the information into each document catalyzes continuous polishing. Each refinement can then be applied across all documents.
- Standardize everything.
  - If you discover a new use case that could potentially be handled by a previous use case, refactor both into a standardized architecture. (Even better, abstract the standardized descriptions up to the highest-possible parent document and hyperlink all child documents up to the parent.)
  - Use consistent formatting. (Headings, spacing, capitalization, etc.) Aside from a clean and professional appearance that indicates credibility, this uniformity is easier on the reader as they switch from document to document.
  - Use consistent naming conventions. (For example, don't call it "Analytics" on some documents, and "Tracking" on others. If something is the same thing, call it the same thing.) The reader should not have to stop and confirm whether two words are a synonym for the same thing, or two different things.

## Process

With the above principles in mind, I typically write my specs in this order:

1. Determine the document (file) nesting.
    1. Plan out the nesting architecture in a Word document using bullet points. These can be cut, pasted, and indented much easier than actual Confluence documents.
    2. The nesting will determine how each document is written, and how they are hyperlinked to each other.
    3. For a website, your nesting could be organized by pathname, or page levels in the data layer. (The two are often closely related, anyway.)
2. Once nesting order is determined, I typically write the parent documents first and work my way down to the child documents.
3. When editing/reading multiple documents, I open each in a new tab. This makes it easier to jump from document to document without wating for each to load, or losing my place in the previous one.
    1. I also organize my tabs the same way every time:
        1. In descending order (from parent to child).
        2. Then chronological order.
        3. Then alphabetical order.
       
       Keeping things in a consistent order develops familiarity, which results in speed.

Of course, this entire process is incredibly recursive. I inevitably traverse up and down this chronology as I continue to discover the abstractions and standardizations I want to make. But following this process keeps such chaos to a minimum.

You can see my [Sample Technical Specs](sample-technical-specs/global.md) here.