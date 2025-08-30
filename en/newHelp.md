# &#128214; Create new help file

1. Go to repository: **[helpTemplate][template]**
2. Click on right top button **Use this template** and **Create a new repository**.
3. Set organization and name your repository according to your needs.
4. Template contains **[CI script][template-CI]**, which you not need to change/update anyhow. In future there can be developed new functionalities which you would like to use in future. In this case you will overwrite CI script manually by copy of it from **helpTemplate**.
5. Clone repository to your local computer:
  ```
  git clone https://github.com/{USER or ORGANIZATION}/{REPOSITORY-NAME}.git
  ```
6. Files: **LICENSE** a **README.md** you can update according to your needs

[template]: https://github.com/HelpViewer/helpTemplate "Help file project template"
[template-CI]: https://github.com/HelpViewer/helpTemplate/blob/main/.github/workflows/publish.yml "CI script"