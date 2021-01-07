---
id: intro
title: Getting Started
sidebar_label: Intro Page
---

## Requirements

The driving force behind the Kisei engine is to provide rapid, iterative rulesets that can be applied actively and retroactively to any number of processes. It should also provide the ability to output the results of queries to the system that can then be interpreted by a graphical display, to allow for easy dissemination of that information.

It should also be scalable, with the ability to apply rules to up to 200,000 people when requested, and allow for the query of those people against the ruleset

## Design Proposal

The foundation of this solution is based on Graph Theory. Quick primer; a graph database is a database that is based on graph theory. It consists of a set of objects, which can be a node or an edge.

- **Nodes** represent entities or instances such as people, businesses, accounts, or any other item to be tracked. They are roughly the equivalent of a record, relation, or row in a relational database, or a document in a document-store database.
- **Edges**, also termed graphs or relationships, are the lines that connect nodes to other nodes; representing the relationship between them. Meaningful patterns emerge when examining the connections and interconnections of nodes, properties and edges. The edges can either be directed or undirected. In an undirected graph, an edge connecting two nodes has a single meaning. In a directed graph, the edges connecting two different nodes have different meanings, depending on their direction. Edges are the key concept in graph databases, representing an abstraction that is not directly implemented in a relational model or a document-store model.
- **Properties** are information associated to nodes. For example, if Wikipedia were one of the nodes, it might be tied to properties such as website, reference material, or words that starts with the letter w, depending on which aspects of Wikipedia are relevant to a given database.

![graph-database](assets/GraphDatabase_PropertyGraph.png)

## Architecture

Kisei is intended to be driven by two Graphs, **People** and **Rules**.

- **People** will primarily be a **Document Store**, with key-value pairs driving **Properties**. It must be easy to continually add Properties to a person within this Document Store.
- **Rules** will be built by adding Nodes and Edges that contain each rule, and will allow a Person and their Properties to traverse that Graph. Once a Persons traversal lands them on a Node, all Edges that relate to that node are possible next steps. Weights/Properties on those Edges determine which of those links to present as a next step for that Person.

# People

![graph-database](assets/gopassport-kisei-arch-people.png)

# Rules

![graph-database](assets/gopassport-kisei-arch-rules.png)

# Assumptions

- The 'Clocking Frequency' of Events will be maintained Server Side, and not Client Side
