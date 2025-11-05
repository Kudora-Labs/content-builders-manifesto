# content-builders-manifesto

This repository holds the **Kudora Builders’ Manifesto** — a living handbook for how we collaborate: principles, ways of working, licensing defaults, decision paths, fork etiquette, and dispute resolution.  
The website reads this repo directly, so anyone can improve the Manifesto through pull requests.

## How to Contribute to the Manifesto

The Manifesto is organized into multiple sections, each as a separate Markdown file in the `sections/` folder. The order and inclusion of sections is managed by the `sections.json` file.

### Editing Sections
- Each section is a Markdown file (e.g., `introduction.md`, `values.md`, `licensing.md`).
- Edit the file using standard Markdown. Keep the first line as the section’s H1 title.
- Do **not** rename files unless you also update `sections.json`.

### Structure and Formatting
- Use headings to organize content:
  - `#` (H1) for the section title (first line only)
  - `##` (H2) for subsections
  - `###` (H3) for sub-subsections if needed
- **Maximum depth:** up to H3. Do not use H4 or deeper.
- Write in clear, direct language. Prefer short paragraphs and lists where helpful.

### Manifest File (`sections.json`)
- The manifest lists all section files in order. Example:
  ```json
  {
    "sections": [
      "introduction.md",
      "principles.md",
      "ways-of-working.md",
      "licensing.md",
      "fork-protocol.md",
      "dispute-resolution.md"
    ]
  }
