---
description: Updates the HTML reference from raw HTML
includeContext: false
arguments:
  - description: force rerun
    required: false
---
/add ./.llm/references.md
- If command arg [{{ARGUMENTS}}] is empty, *AND* if 'last updated' date is today's or yesterday's date, respond *ONLY* with "Tree already updated in the last 24h. Pass argument 'redo' (or anything) to force retry.", and terminate the command. If an argument {{1}} is provided, proceed without terminating.
- Add the "Raw HTML file" reference to context (rawfile)
- Add the "HTML tree file" reference to context (treefile)
- Add the "CSS notes" reference to context (notesfile)
- Analyze rawfile and create a human- and LLM-readable summary optimized for CSS styling projects to quickly recognize the right selectors and properties to modify. Your output should:

1. **Create a visual tree structure** showing the hierarchy of elements with their IDs and classes
2. **Include only CSS-relevant attributes:**
   - `id` attributes
   - `class` attributes
   - Element types (div, span, button, etc.)
   - User-visible text labels (in quotes for context)
3. **Exclude non-styling attributes** like:
   - `data-*` attributes
   - `aria-*` attributes
   - `accesskey`, `loading`, `crop`, `flex`
   - XML namespaces
   - `l10n` references
4. Write the updated tree to treefile.
5. **Modify the "Key CSS Selectors" section** listing the most important selectors for styling, to notesfile.

**Format:**
- Use a tree structure with `├──` and `└──` characters
- Show element type + ID (using `#`) + classes (using `.`)
- Include brief contextual labels in parentheses where helpful

**Example Output Style:**
```
Container Name:

element#id.class1.class2 ("Label Text")
├── child#id.class
└── child.class
    └── grandchild.class
```
- Update the 'last updated' date to today's date YYYY/MM/DD.
- Summarize the changes in the response
- Commit changes to the tree as "LLM updated treeref"