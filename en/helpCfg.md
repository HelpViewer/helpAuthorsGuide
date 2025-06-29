# 🛠️ Help configuration

You can change help configuration in file **_config.txt**. File is located in language version subdir. Each language has its own independent copy.

File structure is:

```
key|value
key|value
```

## Rules

- 1 row = one value
- If the same key will repeat later in the file, the last one value will be used

## Configuration keys

### TOC icons

| Key name | Meaning |
|---|---|
| OverrideBookIcon-opened | Open book character |
| OverrideBookIcon-closed | Closed book character |

### Overwrite user settings of UI

| Key name | Meaning |
|---|---|
| OverrideColorTheme | Overwrites user selection of color scheme and saves it to user's configuration |
| OverrideSidebarVisible | Overwrites user selection if left panel will be visible and saves it to user's configuration |

### Managed by publishing process
| Key name | Meaning |
|---|---|
| _lang | Current help file (package) language |
| _langs | Current help file (package) all languages which were published by pipeline. Used as one of sources of 🌐 list. |
| _version | Released version (took from CHANGELOG.md) |
| _prjname | (organization)/(repository name) in what the help file was present during publishing process. |
