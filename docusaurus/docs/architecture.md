---
id: architecture
title: Architecture
sidebar_label: Architecture
---

## Architecture

Kisei is intended to be driven by two Graphs, **People** and **Rules**.

- **People** will primarily be a **Document Store**, with key-value pairs driving **Properties**. It must be easy to continually add Properties to a person within this Document Store.
- **Rules** will be built by adding Nodes and Edges that contain each rule, and will allow a Person and their Properties to traverse that Graph. Once a Persons traversal lands them on a Node, all Edges that relate to that node are possible next steps. Weights/Properties on those Edges determine which of those links to present as a next step for that Person.

# People

![graph-database](/img/gopassport-kisei-arch-people.png)

# Rules

![graph-database](/img/gopassport-kisei-arch-rules.png)
