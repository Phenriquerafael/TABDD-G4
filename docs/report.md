# Smart Tourism Platform — Project Report

Status: outline awaiting implementation decisions and experimental results. Prompts below identify information required by [the assignment](../Project_TABDD.md); they do not claim that work is complete. Section organization is suggested.

## 1. Application and data

Describe and justify the implemented tourism functionalities: tourist information, geographic exploration, profiles, preferences, favourites, activity history, ratings, comments/reviews, natural-language search, and recommendations.

Describe the dataset, whether real/public/synthetic or combined, its size and characteristics, and its suitability for the application and meaningful indexing analysis. Address the data types considered in the brief.

## 2. Database schemas and models — Part I

For each database below, explain the selected technology and justification; persisted information; organization and relationships; operations; applicable schema patterns considered and used; modelling decisions; and effects on performance, scalability, and maintenance. Justify the distribution of data across systems. Place supporting illustrations in `figures/` and reference them here.

### 2.1 Relational database

Pending — Developer 1.

### 2.2 NoSQL database

Pending — Developer 2.

### 2.3 Vector database

Pending — Developer 3.

## 3. Application architecture — Part I

Pending — shared responsibility.

Identify application components, database roles, communication with the Python application, and interactions between systems. Explain how data distribution supports the main features. Justify decisions in terms of data characteristics, operations, performance, scalability, flexibility, consistency, and query complexity.

## 4. Implementation and integration — Part II

Pending — each developer documents their features; integration is shared.

Explain the functional Python backend, read/write operations across persistence systems, and proof-of-concept frontend. Describe query optimization and index use.

Document at least three distinct implemented functionalities combining information from multiple databases, including one using vector search or recommendations. For each, identify the databases, information exchanged, and resulting application behavior. The proposed flows in the README remain proposals until implemented.

## 5. Semantic search and recommendations

Pending — Developer 3, with contributions from Developers 1 and 2.

Justify the embedding model or method. Explain how application information becomes embeddings, how vectors are persisted and indexed, and how the application uses the vector database's similarity search for natural-language queries. Define and justify the recommendation strategy and the user/content information it uses.

## 6. Indexing experiments

For each scenario, justify its relationship to implemented functionality and realistic usage. Describe the original query without the relevant index; the indexes created/applied; comparative results such as execution time, query plans, logs, or benchmark output; and why the index helps or has limited/negligible impact. Identify the dataset and conditions needed to interpret the comparison.

### 6.1 Relational scenario

Pending — Developer 1. Store queries, index definitions, and evidence in [benchmarks/relational](../benchmarks/relational/).

### 6.2 NoSQL scenario

Pending — Developer 2. Store queries, index definitions, and evidence in [benchmarks/nosql](../benchmarks/nosql/).

### 6.3 Vector scenario

Pending — Developer 3. Store queries, index definitions, and evidence in [benchmarks/vector](../benchmarks/vector/).

## 7. Revisions following Week 9 feedback

Pending — shared responsibility. Describe revisions to Part I following the professor's feedback, if any. Update the preceding sections to reflect the final architecture and models.

## 8. AI-use declaration

AI assistance has been used to summarize the assignment and prepare the initial project plan, documentation structure, team allocation, and report outline. No application code was implemented as part of this documentation task. Update this declaration to reflect any subsequent AI assistance before submission.
