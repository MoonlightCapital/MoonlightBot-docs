# Contributing to MoonlightBot documentation

This repository hosts the official documentation, that can be comfortably viewed on [GitBook](https://moonlightbot.gitbook.io/docs/). Commits to the `main` branch update the documentation on the site instantly.

To ensure the highest standard of quality, all contributions must come in forms of pull requests directed to the `testing` branch. Said branch is connected to [a pre-testing GitBook space](https://moonlightbot.gitbook.io/beta/), to see if in the field everything works as intended before merging into `main`.

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

## Style Guide

* _Always_ add a hyperlink to the command's page when mentioned
* Submit pull requests to the testing branch, not the main branch
* Retain as much information as possible while remaining concise.
  * It can be a difficult balance at times, but mistakes are ok! Pull requests and the testing branch allow for plenty of feedback and revision
* Add additional relevant information when it is missing or improves the section
* Use info hints for information that is indirectly related
* Structure pages and sections in the order a user would need to set the bot up, then use comfortably, then in order of importance
  * I.e., make sure the bot works, then set it to a comfortable language, then continue to moderation set up
* Tables containing specific values, such as the [log names](/advanced/list-of-log-names.md), should be alphabetical
* Command options are listed in the order they appear in Discord, with required ones going first and optional ones after
* Keep the main page as a summary/overview; Add the specifics of a command or feature to the dedicated/relevant page
* New pages need to be added to [SUMMARY.md](/SUMMARY.md), with command pages being sorted alphabetically

Don't forget to communicate! Ask questions and make suggestions. It's ok to be wrong; Learn and try again, we love it! Additionally, your way of thinking might not be immediately clear to others, but that doesn't immediately make it wrong; Even if it's just a gut feeling, let us know why you made the suggestion you did!

### Screenshots

* Add screenshots where relevant, clarifying, needed, etc.
* Use the standardized profile. This is an imitation of the bot owner's profile to maintain professionalism, and is done with her consent.
  * Set your display name to `MoonlightCapital`
  * Set your profile picture to [this image](/.gitbook/assets/ProfilePicture.png)
  * Add a role with the color `#008080` to yourself and the bot
* Compress screenshots (but don't lose quality); [ImageCompressor](https://imagecompressor.com/) is suitable for this
* Keep the outer margins/blank space of screenshots uniform
* Edit out dates, hovered message options, and other visual discrepancies in screenshots
* Use the "Ash" theme, with default spacing/font size/etc.
* Use the official Discord app/client; Do **not** use a modded Discord client for screenshots

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
