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

## Dependency-based blocking

The companion `.github/workflows/blocked-by-status.yml` reads GitHub's native
**blocked by** issue dependencies in this repository:

- An open issue with an open blocker receives `status:blocked`.
- A blocked issue whose recorded blockers are all closed returns to `status:todo`.
- A manually blocked issue with no dependencies keeps its status.
- Pull requests and closed issues are excluded; unrelated labels are preserved.

It runs on issue changes, on a 15-minute schedule, and through **Run workflow** in
GitHub Actions. The schedule covers dependency changes and blockers in other
repositories. It uses the repository's built-in Actions token and needs no new secrets.

CByte reads the labels on its next issue sync and displays the corresponding Kanban
column. That sync also updates Status in the linked native GitHub project. The workflow
itself changes issue labels; it does not directly write GitHub Project fields.

CByte aggregates issues across all repositories configured for a project. Closed
issues appear in Done; open issues with no status label use the linked GitHub project's
Status when available, otherwise Todo. Legacy
`backlog`, `todo`, `in progress`, `blocked`, and `done` labels are also recognized.
Conflicting open-issue labels resolve in this order: Blocked, In Progress, Done,
Todo. Removing a repository from CByte removes its issues from that project's view.

The template source lives in the CByte repository under `templates/github/`.
Only files tracked in `.github/cbyte/managed.json` are updated automatically.
Locally customized managed files and unrelated files are preserved and reported
as conflicts. Reapply defaults from CByte after reviewing a template update.
