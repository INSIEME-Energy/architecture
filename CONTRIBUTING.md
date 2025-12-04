# Contributing to the INSIEME Architecture Document

## How to view the document

There are 2 options to read the architecture documentation:
1. [Visit the architecture website](https://architecture.insieme.energy/architecture/).
2. Set up the architecture website locally by using Node.js 20. 
    - `npm install` to install dependencies
    - `npm run dev` starts serving the website locally

## Notes for editing

The Markdown files are processed using vitepress which support a variety of [Markdowns extensions](https://vitepress.dev/guide/markdown). However, these are the main things to keep in mind:

- **embed images**: Please use markdown syntax `![An example image](./image.png)` to embed images into the page. These will formatted to the text width and include a zoom-in feature automatically.
- **use HTML**: Please avoid using HTML if possible and use Markdown instead. If necessary, all not self-closing tags (like `<p>`) have to be closed to make it compatible with [Vue.js](https://vuejs.org/) templates.

**Editing comments**

To mark pages or sections as outdated, GitHub Alerts can be used to provide these comments. These are used to indicate that a page or section contains questionable or even misleading information. This is a note to the document's reader as well as for the editors to mark sections that need improvement.

```
> [!NOTE]
> Useful information that users should know, even when skimming content.

> [!WARNING]
> Urgent info that needs immediate user attention to avoid problems.

> [!CAUTION]
> Advises about risks or negative outcomes of certain actions.
```
