# Hitman 3 Downpatching

Refer to the HitRuns Wiki Downpatching Guide for Usage Instructions / Patch Notes / Download Links: https://hitruns-wiki.vercel.app/docs/downpatching

- Source code for wiki page [here](https://github.com/solderq35/hitruns-wiki/blob/master/website/docs/downpatching.md)

This repo is just used for hosting the Epic (Legendary) manifest files (see `src` folder), as well as instructions for how to handle game updates (below)

## Game Update Instructions

### Epic Game Version

- Update game version for Hitman 3 on Epic for Legendary. Refer to [instructions specific to Hitman 3 here](https://github.com/solderq35/hitman-tech-tips/blob/main/misc/h3legendary.md#updating-hitman-3), or check Legendary's [general documentation here](https://github.com/derrod/legendary/blob/master/README.md)
- After updating the game in Legendary, find the new Legendary manifest files by going to `%userprofile%` (Windows Search)> `.config` > `legendary` > `manifests`. Or, go to `C:\Users\<username>\.config\legendary` directly

### Steam Game Version

- Update SteamDB Manifest ID's by checking [this page on SteamDB](https://steamdb.info/depot/1659041/manifests/)

### Updating HitRuns Wiki Manifest Download Table

- General Info for official patch notes can be found here: https://ioi.dk/hitman/patch-notes
  - Official patch notes may be missing some stuff, feel free to add some corrections or additions in the table as needed
- Reference [Github Markdown Documentation](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) for general Markdown advice, if needed
- Editing the table directly in Markdown is recommended (Excel does not seem to allow multiple hyperlinks in a table cell, among other UI flaws).
  - I'm using VSCode for editing the Markdown, with [this Markdown extension](https://marketplace.visualstudio.com/items?itemName=starkwang.markdown) for general syntax help, and [this Markdown Preview Extension](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced) to see how my documents will look while still in development.
  - It's recommended to not use word wrapping in your IDE of choice, the Markdown table won't look right if you use wrap.
  - Using [Yarn](https://classic.yarnpkg.com/lang/en/docs/install/#windows-stable), run `yarn install` to install dependencies from `package.json`
  - Then run `yarn prettier` to reformat the data table after editing it (for ease of editing to make columns line up, this doesn't affect how the table looks when compiled)
  - Alternatively, use the Markdown viewer / editor of your choice; https://stackedit.io/ is a solid choice
- If you need to make any major adjustments to the table such as adding a whole column, you can convert Excel to Markdown with following workflow:
  - Make edits to the `h3downpatch.xlsx` file in Excel / LibreOffice
  - Copy contents of `h3downpatch.xlsx` into https://tabletomarkdown.com/convert-spreadsheet-to-markdown/ to convert to Markdown Table.
  - Keep in mind that some links in the table cells may break after you do this.
- Markdown Table of Contents Generator: https://jsfiddle.net/remarkablemark/o0mja3hf/
  - Paste everything from [Purpose and Disclaimer](#purpose-and-disclaimer) and below into the jsfiddle and it'll spit out a table of contents
  - Including the first header `#Hitman 3 Downpatching` will make the table of contents unnecessarily nested
- Good idea to run `yarn prettier` before you make a commit in general, it can fix a lot of Markdown formatting issues
