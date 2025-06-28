# 🛠️ Viewer Custom UI

## Full override

1. In **HelpViewer** dir inside file **hvdata/data.zip** you will find these files:
| File | Meaning |
|---|---|
| layout.htm | UI HTML code |
| appmainNext.js | Business logic |
| main.css | CSS style |

1. Extract them
2. Create directory **_base** in root directory of help file repository (as same level as directories with language versions)
3. Copy these files to **_base**
4. Do your desired changes here in these files

## Pure extension

If you only want to add some new functionality, then you can add these files to **_base**:

| File | Meaning |
|---|---|
| plus.css | CSS style which extends or overrides current ones |
| plus.js | Extension of business logic of HelpViewer |

## Result

1. During help publishing there will emerge another archive file **Help-.zip**
2. You need to add this file to your help file distribution. Otherwise changes will not have any impact
3. Your changes will not interfere HelpViewer installation on user computers. It will change only user work mode exactly with help file to whom you will attach these changes

## Work with help file

- When viewing a help file, users need to access the help file in the format: **Help-__.zip**, for HelpViewer to try to search for this new file with changes
- If there is used exact language directly, then HelpViewer will search for these changes inside this help file (and according to distribution process it will not find them here)
- If users will be somewhat limited by your changes, then it will be enough to them to remove file **Help-__.zip** and they will be able to regain back usual functionality of HelpViewer

## 💡 Recommendations
- Source code of interface (unzipped files) can be your inspiration for your own customization
- Ensure if you are implementing usual features which are behaving standard way
- It is desirable that id names of html elements are stable (and also not missing) because of further business logic (you are not changing here) relies on them. You are using all of this logic but in other scenarios you are defining them here
- Further business logic of HelpViewer outside these named files cannot be changed straightly by help file. There is needed to perform HelpViewer source code change if another changes are required.
