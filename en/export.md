# 📥 Export

The 📥 Export button (on the right side of the top panel above the chapter text) allows you to export the chapter text into several formats.

## Formats

- **HTM**  
  One [HTML][HTML5Syntax] page with all chapter content (single book principle)
- **MD**  
  [markdown][MDSyntax] source code
- **TEX**  
  [LaTeX][LATEX] source code for subsequent output to **PDF**
- **EPUB**  
  ePub e-book format compatible with ePub2 and ePub3  
  (tested primarily on SW readers - [EPUBReader][EPUBReader] (Chrome), also on Android - [ReadEra][readera], [eBoox][eboox])  
  If no list of topics is available, the export module will attempt to create one from the **h1** headings in the chapters.
- **RTF**  
  - Source code is compatible with **Word 97 (RTF 1.5)** and higher
  - Text formatting functions are used only to a basic extent (despite your HTML can be more rich in format)
  - Headings are correctly defined but without any special format (you can easily change style template in Word afterwards)
  - Output from **Prism** is printed in "typewriter" font (no colors and format)
  - Output from **Marked** is skipped
  - Uses default **ANSI codepage** (East Europe and other languages exports may have malformed letters with diacritics)
  - Images are not imported
  - Tables are imported via texts with tab spaces
  - Unicode characters are malformed, but inserted
- **STATIC**  
  A set of HTML pages that are:
  - static,
  - minified,
  - linked to each other by relative URI paths,
  - supplemented with SEO metadata (og*:, description),
  - CSS styles and HTML structure are still compatible with **HelpViewer** (reusable custom styles for HelpViewer without the need for further modifications),
  - UI elements are reduced to basic hyperlinks (icons are taken from buttons at the time of export),
  - inspired by the principles of the WCAG 2.1 AA accessibility standard,
  - 💬 Texts and tooltips on buttons and other elements are taken from the active localization at the time of export,
  - do not contain JavaScript from the **HelpViewer** application logic and do not require the application to run,  
    JavaScript from the help chapters that the author has inserted into the text is included.  
    JavaScript referenced in the head section is not included.
  - CSS styles of external components (Mermaid, Prism) are included, JavaScript is omitted.
  - If no list of topics is available, the export module will attempt to create one from the first **h1** headings of each chapter.
  - Optionally, it is also possible to include the export of the list of 📇 [keywords][Dkeywords.lst] or the list for 🔎 [full-text search][fulltextIndex]
  - Export limitations:
    - ✨ **Intro screen**, 💧 **Watermark** are not included in the export.
    - 🌐 Languages - only the active language version is exported. Switching between languages will not be possible.
  - Support for custom modifications:
    - The empty **src/custom.css** file allows you to add any necessary CSS style modifications after export.
    - In the **sitemap.xml** and **robots.txt** files, replace **\_REMOTEHOST\_** with the full URI of your target domain where you will deploy the pages.

## Limitations

- Exports always work only with the visible text of the chapter. The exception is lists in **STATIC** exports.
- The administrator can install the application without some export formats.
- The administrator can completely remove the function from the installation - the button will then be missing.

## Synergies

- In combination with the 📚 Display all chapters as **one document** function (the administrator can also remove this from the installation), you can export the entire documentation.  
  Where appropriate, the export process uses the configuration options selected here.  
  The functions complement each other, but both do not need to be installed in the application.  
  The **Static: Export dictionaries** option determines whether keyword and full-text lists will also be exported (exporting them significantly increases the file size).
- In combination with the 🖨️ **Print** function, it is possible to remove [unicode icons][IconPrint] from the text of chapters using the following procedure:
  1. In the **single document** function, select the **Remove** option in **Print icons**.
  2. Click **Print** to display a preview before printing, which you should cancel (do not send to the printer).
  3. The icons will be removed and the exports will work with the visible text of the chapter.
- The 🖨️ **Print** function normally allows you to print a page to **PDF** in modern browsers.
- In combination with the [👀 View Repository][viewRepo] function, you can read freely available external sources (for example, a free set of linked md files).
- Using the **d** parameter in the URI ([?d=https://helpviewer.github.io/][test]), freely available external resources can be read.

[MDSyntax]: https://www.markdownguide.org/basic-syntax/ "MD"
[HTML5Syntax]: https://www.tutorialspoint.com/html5/html5_syntax.htm "HTML"
[LATEX]: https://www.latex-project.org/ "LaTeX"
[EPUBReader]: https://chromewebstore.google.com/detail/epubreader/jhhclmfgfllimlhabjkgkeebkbiadflb "EPUBReader"
[readera]: https://play.google.com/store/apps/details?id=org.readera "ReadEra"
[eboox]: https://play.google.com/store/apps/details?id=com.reader.books "eBoox"
[Dkeywords.lst]: mdata/keywords.lst.md "📇 Keywords list (keywords.lst)"
[fulltextIndex]: fulltextIndex.md "🔎 Fulltext search (fts-keywords.lst)"
[viewRepo]: :viewRepo.htm "👀 View your repository"
[test]: ?d=https://helpviewer.github.io/
[IconPrint]: texts.md#h-2-0 "Unicode icons"
