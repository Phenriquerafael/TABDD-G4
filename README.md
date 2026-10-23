# TABDD-G4 — Smart Tourism Platform

Project plan for three developers, based on [the assignment brief](Project_TABDD.md). The requirements below come from that brief. Folder names, report organization, team allocation, and proposed integration flows are team planning suggestions, not additional assignment requirements.

## Assignment requirements

- Build a Python tourism application with a functional backend and proof-of-concept frontend.
- Support destination and point-of-interest browsing, geographic searches, profiles, preferences, favourites, activity history, ratings, comments, and review management.
- Support natural-language semantic search and a justified recommendation strategy.
- Use at least three persistence systems: relational, NoSQL, and vector. Justify technology choices, schemas, data distribution, and architecture.
- Generate, persist, index, and search embeddings through the vector database; in-memory-only similarity search is insufficient. Justify the embedding model or method.
- Implement at least three distinct features combining multiple databases, including at least one involving vector search or recommendations. Optimize queries.
- Use data suitable for the features and sufficiently large for meaningful performance and indexing analysis. Consider structured, semi-structured, geographic, preference, interaction, review, and semantic-search text data.
- Analyze one indexing scenario for each paradigm: relational, NoSQL, and vector. Describe the original query without an index, apply appropriate indexes, present comparative evidence, and explain significant, limited, or negligible benefits. Scenarios must represent implemented features and realistic usage.

## Deliverables and dates

| Milestone | Required work | When |
| --- | --- | --- |
| Part I discussion | Present database schemas, modelling decisions, technologies, and architecture to the professor for formative feedback | Week 9 |
| Final delivery | Detailed report covering Part II implementation and indexing analysis, plus any revisions to Part I following feedback | 8 December 2026, 23:59 |
| Oral presentation | Discuss implementation, technical decisions, and indexing scenarios and results | Weeks 13–14 |

The brief does not provide calendar dates for the teaching weeks or a timezone for the deadline. Week 9 feedback is not final approval of the design.

Reports must be submitted in a ZIP named `ClassQ_Branch_xxxxxxx_yyyyyyy_zzzzzzz.ZIP`, using the class, MEI specialization track, and three student numbers. Late submission incurs a 10% penalty per day. A member absent at the assigned presentation receives zero. AI assistance must be declared when used.

## Documentation organization

```text
TABDD-G4/
├── Project_TABDD.md          # Original assignment brief
├── README.md                # Requirements, dates, and proposed team plan
├── docs/
│   ├── report.md            # Detailed report outline
│   └── figures/             # Supporting model/architecture illustrations
└── benchmarks/
    ├── relational/          # Queries, index definitions, comparative evidence
    ├── nosql/
    └── vector/
```

Complete the [report](docs/report.md) with actual decisions and results as development proceeds. Store experiment evidence in the corresponding benchmark folder and reference it from the report. `.gitkeep` files only preserve empty folders in Git. This structure and Markdown format are suggested; separate meeting notes, decision records, AI-use files, and slide decks are not explicitly required.

## Proposed team division

Developer numbers are placeholders for the three team members. Database ownership below is a proposal to justify in Part I, not an assignment-prescribed data model.

| Owner | Implementation, including associated interface flows | Report contribution | Indexing experiment |
| --- | --- | --- | --- |
| Developer 1 — Relational | Profiles, preferences, favourites, ratings, comments, and reviews | Relational model, operations, decisions, and related functionality | Representative relational query before/after indexing |
| Developer 2 — NoSQL | Tourism catalogue, geographic exploration, and activity history | NoSQL model, dataset characteristics, operations, and decisions | Representative NoSQL query before/after indexing |
| Developer 3 — Vector | Embedding generation/persistence, natural-language search, and recommendations | Vector model, embedding method, search, and recommendation strategy | Representative vector query before/after indexing |

### Proposed cross-database features

| Feature | Integration | Owners |
| --- | --- | --- |
| Semantic search | Vector matches enriched with NoSQL destination details | Developers 3 and 2 |
| Favourites | Relational favourite records enriched with NoSQL destination details | Developers 1 and 2 |
| Recommendations | Relational preferences combined with vector similarity and NoSQL content | All three |

### Shared responsibilities and dependencies

- Agree together on architecture, database responsibilities, shared identifiers, and data exchanged between features before parallel implementation.
- Developer 3 depends on Developer 2's searchable content and Developer 1's preferences. Developer 1 depends on destination identifiers/details for favourites and reviews; Developer 2 needs shared user identifiers for activity history.
- Each developer completes their feature integration, model explanation, and indexing analysis. All three share frontend integration, query optimization, report assembly, and presentation preparation.
- Prepare Part I for Week 9, build an integrated search flow early, complete remaining features and experiments, then finalize the report and rehearse the presentation. Record any feedback-related design revisions in the report.
