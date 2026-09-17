# Documentation Writing Procedure

This guide contains all you need to know to perfectly work on the MoonlightBot documentation.

As a Documentation Writer, your mission is to keep the documentation up to date and improve its readability. By doing a good job, more people will use MoonlightBot and join our volunteer programs.

## The Development Cycle

The development cycle ensures updates are tested and documented before going live.

1. **Monitor `#test-todo`**: Check for new releases sent to testers.
2. **Analyze Changelogs**: Read changelogs and understand what needs to be documented.
3. **Assign Tasks**: Go to the GitHub project board. If you have time in the next 10 days, are not doing another task, and the task is unassigned, click "Add assignees" to take it. Move it to the "In Progress" column.
4. **Test Updates**: Try the updates on the MoonlightBot test instance to understand them.
5. **Write Documentation**: Create necessary pages or update existing ones. Use `/test generate-doc-page` on the bot to generate the base Markdown for command pages (internal order is preferred over alphabetical).
6. **Submit PR**: Create a Pull Request with your changes for review.
7. **Address Feedback**: Managers and developers will review your PR. Address their changes.
8. **Celebrate**: Once merged, you did it!

## Branching and Writing

- Always start on a clean slate by making a new branch based off the `testing` branch.
- Name your branch meaningfully, e.g., `v4.7-additions` or `expand-faqs`.
- When updating commands, remember that you have the full power of Markdown. Don't limit yourself to Discord's description limits.
- Make sure to update `SUMMARY.md` if you are adding new pages so they appear in the sidebar.

## Pull Requests and Reviews

Your pull request will be reviewed by managers and the developer. They will check if the page is understandable, formatted correctly, and free of typos. You are expected to monitor GitHub notifications and fulfill their requests.

Once approved, it will be merged into the `testing` branch, and eventually to `beta` and `main`.
