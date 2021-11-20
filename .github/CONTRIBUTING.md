# Contributing to MoonlightBot documentation

This repository hosts the official documentation, that can be comfortably viewed on [GitBook](https://moonlightbot.gitbook.io/docs/). Commits to the `main` branch update the documentation on the site instantly.

To ensure the highest standard of quality, all contributions must come in forms of pull requests directed to the `testing` branch. Said branch is connected to [a pre-testing GitBook space](https://moonlightbot.gitbook.io/moonlightbot-documentation-preview/), to see if in the field everything works as intended before merging into `main`.

## Project structure

NOTE: This is heavily based on findings and supposition. This section is subject to change as more understanding of the GitBook integration is discovered.

* `README.md` is the home page
* `SUMMARY.md` is the representation of the summary bar in the GitBook interface, with the links and dividers
* The `.gitbook/assets` folders contain all images and other assets to be displayed in the documentation
* For each section of the guide (as shown in level 2 headings of the summary), there's a folder. Folder names are all in lowercase, and each word is separed by a dash (`-`)
* Pages are Markdown files that follow the same naming convention as the folders, just with a `.md` extension
  * For pages that have a main page with content and sub-pages, the main page is the `README.md` of the folder, and the rest of the sub-pages are in the same folder, named like normal

## Special Markdown

GitBook uses its own set of special markdown for displaying structures like hints and tabs. This is most likely not rendered by many WYSIWYG editors, so extra care must be put to ensure they work correctly.

### Hints

Hints are those boxes with a colored bar and an icon meant to catch the reader's attention on important points.

All hints start with `{% hint style="HINT_STYLE" %}`, where `HINT_STYLE` can be any of the following:

* `info` (blue) for informative messages
* `success` (green) to indicate success of an operation
* `warning` (orange) to tell the user they should be careful about the contents of the hint
* `danger` (red) to signal a dangerous operation that may be potentially be disruptive if disregarded

To end an hint box, use the `{% endhint %}` tag.

### Tabs

Tabs are boxes of content that show a list of tab titles, and the reader can view the content of each tab by clicking on the title. They can be used for a compact page layout for repetitive content.

To start a group of tabs, use the `{% tabs %}` tag. For each single tab, wrap them in `{% tab title="TITLE" %}`, replacing the title accordingly, and `{% endtab %}`. End the whole group of tabs with `{% endtabs %}`.

## Commit and branch naming

Try to keep the names of branches and commits meaningful.

Ideally, branches should be named after what the scope of the changes is (for example, documenting the creation of a command named "massban" could be named `massban-command`), and commit messages should describe briefly what changes were made in that commit.

## Pre-release and beta content

Features in beta can (and should) be added to the documentation. They must cite the minimum available version and how to get access to beta, which will then be removed once the feature reaches stable. Pull requests about changes that are still pre-beta can still be made, but the requests will be held until they're deployed to beta.

## Policies

**Under no circumstances anyone who is not Moonlight Labs Staff is allowed to make changes to the Acceptable Use Policy or Privacy Policy.** This includes grammar corrections. Any pull request editing the policy files that is not officially licensed will be closed.

## Typos and minor edits

Albeit all the reviews required before merging a pull request into the main branch, there are chances that typos or formatting errors still pass through.

Please refrain from opening pull requests just to make a single, minor correction. You may still make pull requests that are about general, project-wise minor improvements.

To report any inconsistency that may have slipped through the review process, or are being overlooked on an open pull request, contact a helper in the [Discord server](https://discord.gg/hNQWVVC), or comment on the pull request itself.
