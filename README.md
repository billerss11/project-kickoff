# Project Kickoff

A Codex skill for starting small business projects with clear context, useful folders and practical document control.

It works from a conversation, a few files or an existing collection. When context is missing, it asks focused questions before choosing the setup. It writes three concise, populated documents:

| Document | Purpose |
|---|---|
| `AGENTS.md` | Brief project identity and project-specific operating and maintenance rules. |
| `Project Guide.md` | Current position, folder map, working references and next actions. |
| `Document Log.md` | A concise diary of material events, decisions and evidence. |

Folders and additional records depend on the work. The skill supports RFQs, supplier quotations, proposals, service work and internal initiatives without prescribing one industry or management system. It preserves existing useful conventions and distinguishes received originals, working material and actual issues.

## Install

Clone this repository as `project-kickoff` under your Codex skills directory. With the default location:

```powershell
git clone https://github.com/billerss11/project-kickoff.git "$HOME/.codex/skills/project-kickoff"
```

If you configured `CODEX_HOME`, use its `skills` subdirectory instead. Use a fresh destination; do not overwrite an existing skill. Start a new Codex session if the skill is not yet listed.

## Use

```text
Use $project-kickoff to initialize the project in [project folder].
We are preparing a service proposal for a customer. I will maintain
the records with AI. We have an initial request but no supplier offers.
Read the request, ask for missing background, and set up the project.
```

An empty-folder request is equally valid. Explain the objective and your role; the skill gathers the other essentials. Discussion-only requests remain discussions. Normal automatic skill discovery is enabled.

Generated project files belong in your project directory, not in this skill repository. The skill does not publish project material, contact parties or initialize Git unless that work is separately requested.

## Maintain with Git

The installed directory is an ordinary Git checkout. Review and commit intentional edits there, then push them to your repository. To retrieve remote changes when your local work is clean:

```text
git pull --ff-only
```

The entry point and core document contracts are in [SKILL.md](SKILL.md). Read only the relevant sections of [Project controls](references/project-controls.md) for complications such as partial revisions, multi-party exchanges and release packages. Current actions belong in the guide, historical decisions in the log, and stable operating rules in AGENTS.md. Link to supporting detail instead of repeating it.

When changing the skill, check behavior on an empty project, a project with limited conflicting source material, and a simple internal project without suppliers. Confirm that it asks useful questions, writes real context, preserves sources and avoids unnecessary records. Validate the frontmatter with the skill-creator validator available in your Codex installation.
