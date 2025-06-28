# 📑 Heading detection

💡 Recommendation:
- Each chapter should start with h1 (1x #) heading which will be the 1st one heading and text on the start of the document.

**HelpViewer** resolves document heading in this order of priority (from most significant):
- **h1** heading text form chapter text if it is on the start of the document text (skips next points lower here)
- TOC item text (📖) when clicked
- Dictionaries item text (📇, 🔎) when clicked.  
This serves as a backup heading text. It is also preferred when the user reloads the page.
- Relative path and file name inside help file
