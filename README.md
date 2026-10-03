# Agile Today methodology graph

The descriptive layer of the [Agile Today](https://agile-today.org) methodology graph: practices, techniques, events, artifacts, roles, stages and gates of project management, business analysis and systems analysis, the typed links between them and the sources they come from. Every node is in English and Russian.

The same data is served at https://agile-today.org/api/graph. Decisions on top of it — project routes, gate verdicts, plan checks — come from the Agile Today MCP server at `https://agile-today.org/api/mcp` (free, no sign-up; [how to connect](https://agile-today.org/en/mcp)). This repository holds the data only: the decision rules and the engine are not part of it.

## graph.json

| Field | Meaning |
|---|---|
| `version`, `released`, `content_hash` | the release of the graph |
| `layer` | always `descriptive` |
| `license` | the license and attribution line |
| `counts` | totals of nodes and links |
| `nodes` | 425 nodes: `id` (e.g. `a.rollback_plan`), `t` (type: practice, technique, event, artifact, role, stage, gate, school, model, tool, law, antipattern, stream, scenario), `n` and `d` (name and description, `en` and `ru`), `src`, `src_type`, `sl` and `lvl` (the source and its level) and type-specific fields |
| `edges` | 2462 links: `id` (`Lxxxx`, stable — cite it), `f` (from), `t` (link type), `to` |

Link ids never change and are never reused, so `L0421` keeps pointing to the same statement across releases.

## Use and attribution

Licensed under [CC BY 4.0](LICENSE): you may copy, adapt and share it, also commercially. Credit it as:

> Agile Today methodology graph by Oleg Vakarchuk, https://agile-today.org, licensed under CC BY 4.0

The name "Agile Today" and its logo are trademarks and are not licensed: see [TRADEMARKS.md](TRADEMARKS.md). Names of methodologies and standards belong to their owners; the graph names and links concepts and does not reproduce the text of the standards.

## Corrections

A wrong link, source, description or translation? Open an issue — see [CONTRIBUTING.md](CONTRIBUTING.md). `graph.json` is exported from the private source of the graph, so pull requests are not merged directly; accepted corrections ship in the next release.

## Releases

Each graph version is one commit and a tag, for example `v2.3.0`.

---

**По-русски.** Описательный слой графа методологий Agile Today: практики, техники, события, артефакты, роли, этапы и гейты управления проектами, бизнес- и системного анализа, связи между ними и источники — на английском и русском. Лицензия CC BY 4.0 с указанием авторства (строка выше). Решения — маршрут проекта, вердикты по гейтам, проверку плана — даёт MCP-сервер `https://agile-today.org/api/mcp`; правила решений и движок в этот репозиторий не входят. Ошибку в данных можно сообщить через issue.
