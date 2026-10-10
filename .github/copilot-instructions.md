# Copilot instructions

## Repository purpose and structure

This repository is a Markdown/Obsidian vault for a *Call of the Netherdeep* D&D campaign, not an application. Treat all campaign material as spoiler-bearing; the repository is intended to be shared with the DM, not the other players.

The tracked notes have distinct roles:

- `Adventure-Notes/Session-Notes/` is the chronological record of play. Name new files `Session <number>.md`.
- `Adventure-Notes/Dramatis personae.md` is the campaign-wide character index. Keep PCs and NPCs in their existing tables, including location, pronunciation, player, and notes where applicable.
- `Adventure-Notes/Quests.md` is the campaign-wide quest summary, divided into main and side quests.
- `Characters/Ideas/` contains pre-campaign character concepts rather than session history.
- `README.md` is the navigation entry point. Add links there when introducing another major note collection.

When session notes introduce or materially change an NPC, PC, or quest, update the relevant campaign-wide index as part of the same change rather than leaving that information only in the session file.

## Markdown conventions

- Use body-only Markdown; existing notes do not use YAML front matter, tags, or generated metadata.
- `Private/Lore/` is the sole exception: its local workflow may require YAML front matter for structured lore metadata.
- Use standard Markdown links. Every relative link must resolve to a file; link collections through an explicit index file such as `README.md`, never a directory. Wrap link destinations containing spaces in angle brackets, for example `[Dramatis personae](<../Adventure-Notes/Dramatis personae.md>)` from this file.
- Session notes begin with `**Session Date : <date>**`, followed by `### Start of Session Context`, `### Mid Session Notes`, and `### Wrap up Notes`.
- Character ideas use the `## Theme`, `## Surface Demeanor`, and `## Backstory Overview` sections. The theme starts with a short italicized phrase before the supporting prose.
- Preserve the existing table schemas in campaign-wide indexes when adding rows; extend a schema only when the new field is useful across multiple entries.

## Privacy and ignored vault state

- Put notes that must not be committed publicly under `Private/`. Everything there is ignored except `Private/README.md`; never move private details into tracked notes merely to make them visible to Git.
- `Private/Lore/` is the ignored local Exandria lore library. Before researching or answering an Exandria lore question, read `Private/Lore/README.md` when it exists and follow its retrieval, provenance, spoiler, and campaign-canon rules. In-session lookups are local-only unless the user explicitly requests research.
- `.obsidian/` and `Templates/` are intentionally ignored local vault state. Do not force-add them or make tracked content depend on a particular local Obsidian configuration or template.
