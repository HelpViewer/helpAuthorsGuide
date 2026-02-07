# 🏷️ Branding your help file

To customize the default identity of the application to your own visual identity, **HelpViewer** provides tools that are described in the following subchapters.

For some tools, simply adding files to your help is sufficient. For others, configuration changes or knowledge of CSS or JavaScript is required.

For the changes to be visible to users, you must always recompile the help (release a new version). Otherwise, the new files or CSS/JS changes will not be visible.

## Easy modifications

### 🌅 First screen

- The first screen is represented by the **README.md** file located at the root of the language version of the help.
- This file opens first when the reader launches the help.

### 🌐 Custom application icon in the page header (favicon)

- Place the file in the help repository:
**helpProject/_base/favicon.png**

### 📖 Topic tree icons

- The option to change icons in the topic tree is described in the chapter [TOC icons][TocIcon].

## Configuration edits

### 🎨 Replacing or extending cascading styles

- How to replace or extend cascading styles is described in the chapter 🛠️ [Viewer Custom UI][customUI].
- Keep in mind that some definitions (e.g., CSS class names or id attribute values) can only be changed with certain restrictions.
- In the file hvdata/data.zip:**main.css**, there is a pseudo-class **:root** at the beginning, which contains color palette constants. For initial adjustments, changing the values here may be sufficient.
- Within the pseudo-class **:root**, which you would define in **plus.css**, you can additionally change the font of the entire application interface.
- CSS3 allows you to define [visual effects and transitions][CSS3Effects]. Another source can be the article [Web Visual Effects with CSS3][CSS3Effects2].

#### 🖌️ Changing colors and fonts

Below is an example of how to set global variables for colors and fonts. You can then use these variables anywhere in CSS via `var()`.

```css
:root {
  --color-bg: black;
  --color-fg: white;
  --font: "Segoe UI", Roboto, sans-serif; /* main font */
}

body {
  font-family: var(--font);
  background: var(--color-bg); /* use of variable */
  color: var(--color-fg, silver); /* use of variable with fallback value if missing */
}
```

If possible, use CSS variables. This makes it easier to change colors, fonts, or other parameters in the future.

#### 🖱️ Defining a custom cursor

- You can define a custom cursor in **plus.css** as follows:

```css
:root {
  cursor: url('my-cursor.png'), auto;
}
```

The file **my-cursor.png** must be in a relative location to **index.html** and cannot be part of help files or data (it cannot be in a ZIP archive).

#### ✨ Splash screen

- The splash screen fills the entire visible area and is used for quick presentation - typically a product icon, name, and short slogan. - Place the following file in the help repository for each language:
**helpProject/(language)/_splash.md** :

```markdown
# _![HelpViewer](media/HV.png)

# HelpViewer

## Your help - Clear - Fast - No compilation
```

(the underscore in the first heading means do not remove the definition for the pTR1stHeadingToTopPanel plugin)

- If 🖥️ puiSplash (Start Screen) is included in the deployed application package, this screen will be the first information displayed to the user when they first open 🌅 the first screen.

- To customize its appearance, you need to define **helpProject/_base/plus.css** and include, for example, the following:

```css
.splash {
  gap: 3rem;
  font-size: calc(1em * 1.5);
  background: radial-gradient(circle, var(--c-contentPaneColor) 10%, var(--c-backgroundHead) 100%);
}

.splash h2 {
  text-align: center;
  word-wrap: break-word;
  overflow-wrap: break-word;
  hyphens: manual;
}
```

### 🧩 Advanced tools, programming

- Some tools in the following chapters may be limited or non-functional depending on the deployment or configuration in your environment. For information on downloading and installing the package, contact your system administrator.
- The tools require minimal configuration. Some require additional programming of the source code when running the help (helpProjekt/_base/**plus.js**).
- These advanced options for modifying the application identity are described in 🧩 [Developer Guide][DGuide].
- Automatically generated documentation of the running instance is also available and accessible via the 🧩 [Object explorer][oexplorer] plugin in 🐞 debug mode. Debug mode is not enabled by default in production environments.
- The application can be downloaded as:
  - 🚀 complete package (ZIP)
  - 📥 custom package (ZIP)
  - 🐳 [Docker/Podman container][DCONT]

### 💧 Watermark

- Functionality is provided by the 🖥️ puiWatermark plugin (Watermark on content pane), which must be supplemented with configuration.

### 🖼️ Custom icons for buttons

- Button icons can be changed in the configuration of plugins derived from 🖥️ puiButton. Each plugin has a configuration option ⚙️ CAPTION with a default value.
- To change the icons, you may need to distribute your own font file within the help file (place it in the **_base** directory).

### 💬 Texts and tooltips

- Application labels and translations are controlled by localization, which is part of the application data.
- For more information, see the following chapters:
  - 🌐 [New language for Viewer][DGuideLangCentral] - main localization data
  - 🌐 [Plugin localization][DGuideLangPlug] - localization data for individual plugins
- These changes only require configuration adjustments. Code modifications are usually not necessary.

#### © Copyright, ® registered, and ™ trademark

- Copyright, registered design, trademark, and disclaimer texts must be added to the application according to your needs.
- Program-level support for this area is not significant.
- Programming and manual modification or extension of the application package is required here.
- The application is distributed under an open license [MIT][MIT]. You can modify and distribute the code commercially and non-commercially, but you must retain the **HelpViewer** license and the original copyright in your own packages.

The following procedure is an example of a possible implementation with minimal programming:

1. Activate the plugin in **helpProject/_base/plus.js**:

```js
activatePlugin('puiHeader', 'Down', STO_HELP);
```

2. Define the configuration in **helpProject/_base/plugins-config/puiHeader_Down.cfg**:

```text
POSITION|b
TEXT|(C) ACME, 2025
ARIAHEADER|contentinfo
```

This activates a new instance of the **puiHeader** plugin named **Down**. At the same time, it is necessary to create a configuration file with the exact name specified so that the configuration is loaded automatically. The result will be a new panel located below the chapter content panel, which will display the text from the **TEXT** key. This text will always be displayed to the user on the screen and will be included in the print output, for example. The **ARIAHEADER** key specifies the accessibility role of the content.

###  Custom admonition block type

As part of the information blocks (admonition) solution, you can define your own type according to the instructions in the chapter 🛠️ [Viewer Custom UI][customUI] and also in this way in **custom.css** in the help:

```css
:root {
  --c-border-note-mytest:rgb(207, 207, 34);
}
.note-mytest {
  border-color: var(--c-border-note-mytest);
}

.note-mytest p::before {
  content: "MT ";
}
```

using the same method as for other types:

```markdown
> [!MYTEST]Block of unknown type
```

[TocIcon]: tocIcon.md "TOC icons"
[customUI]: customUI.md "Viewer Custom UI"
[DGuide]: ?d=hlp-dguide/Help-__.zip "Documentation for developers"
[DGuideLangCentral]: ?d=hlp-dguide/Help-__.zip&p=newLangViewer.md "New language for Viewer"
[DGuideLangPlug]: ?d=hlp-dguide/Help-__.zip&p=plugLocStrings.md "Plugin localization"
[oexplorer]: ?d=hlp-dguide/Help-__.zip&p=oexplorer.md "Object explorer"
[DCONT]: https://github.com/HelpViewer/HelpViewer/pkgs/container/helpviewer "Container"
[CSS3Effects]: https://prismic.io/blog/css-image-effects "50 Creative CSS Image Effects for Engaging Websites"
[CSS3Effects2]: https://leanpub.com/web-visual-effects-with-css3/read "Web Visual Effects with CSS3"
[MIT]: https://github.com/HelpViewer/HelpViewer/blob/master/LICENSE "MIT license"
