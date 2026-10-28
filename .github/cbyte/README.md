# CByte project defaults

This repository participates in its CByte project's Timeline, Kanban, and Duty Board.
The project link and shared configuration live in `.github/cbyte/project.json`.

| Label | Column |
| --- | --- |
| `status:todo` | Todo |
| `status:in-progress` | In Progress |
| `status:blocked` | Blocked |
| `status:done` | Done |

Use one status label per issue. The CByte status workflow assigns Todo to new
issues, assigns Done when an issue closes, and resets Done to Todo on reopening.
Changing a status label to Done closes the issue; choosing another status reopens
it. Other labels and existing repository workflows are preserved.

CByte aggregates issues across all repositories configured for a project. Closed
issues appear in Done; open issues with no status label appear in Todo. Legacy
`backlog`, `todo`, `in progress`, `blocked`, and `done` labels are also recognized.
Conflicting open-issue labels resolve in this order: Blocked, In Progress, Done,
Todo. Removing a repository from CByte removes its issues from that project's view.

The template source lives in the CByte repository under `templates/github/`.
Only files tracked in `.github/cbyte/managed.json` are updated automatically.
Locally customized managed files and unrelated files are preserved and reported
as conflicts. Reapply defaults from CByte after reviewing a template update.
