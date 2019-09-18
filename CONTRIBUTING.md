# Contributing to the documentation

This documentation can be freely edited through the git system. Here are some guidelines to follow while making contributions:

- **Have a clear, comprehensive title and description:** this will help developers and future contributors understanding what changes you've made.
- **Proofread what you write:** while it's true you can correct grammar mistakes and typos in a later commit, this helps keeping the repo history clean.
- **Keep command usages and examples in `single line codeblocks`**, also, follow the guide indication for parameters.


## File and folder structure

Since this documentation will be read and parsed by a script, you are required to follow a specific structure while adding sections or pages.

Every page goes inside the /docs folder, and any image used in the documentation must be uploaded in docs/images. **You must not link to any third party site for image hosting for any reason.**

It is strictly forbidden to add any tracking in pages.

Subfolders of the /docs folder are treated as sections, and may contain other pages.
Pages are markdown files, ending with .md extention.

Both subfolders and pages are **case-sensitive**, which means that, for example, `Getting-started.md` and `getting-started.md` are two different pages.

Since both folder and file names will be shown to end users in the docmuentation as page/section names, there are a few rules to follow:

```
docs/1.Getting-started/1.Adding-the-bot.md >>> Getting started - Adding the bot
```

Dashes are replaced with spaces, also, since the script sorts files in an alphabetical order, please put a number before the page/category name.

`docs/Welcome.md` is forced as the starting page.
