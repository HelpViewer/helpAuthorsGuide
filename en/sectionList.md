# 🔖 Sections List

**HelpViewer** automatically assembles a list of sections (🔖) based on the document's headings (h1-h6, i.e. # ... ######), providing users with a quick and convenient way to navigate through the chapter.

## Visibility conditions

- If the document contains only a main heading (h1 / #), the list will not be shown.
- The list becomes available as soon as there is at least one additional heading of any level (h1-h6).

## Naming Format of Anchors

Headings are automatically named in the following format: #h-(level)-(order).
  - level is a number from 1 to 6 indicating the heading level (h1 = 1, ..., h6 = 6)
  - order is a zero-based index that reflects the heading’s position among headings of the same level across the entire chapter.

## Determining Anchor Order

- Each heading level has its own counter (h1, h2, ..., h6 are tracked separately).
- Headings are indexed in the order they appear - left to right, top to bottom.

## Handling Changes in Document Headings

⚠ If a new heading is inserted between two existing ones, it inherits the index of the heading that originally occupied that position. All subsequent headings at the same level are automatically shifted.

This ensures that anchors remain consistent and predictable, even as the document structure evolves.
