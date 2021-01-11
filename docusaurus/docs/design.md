---
id: design
title: Design
sidebar_label: Design Proposal
---

## Design Proposal

The foundation of this solution is based on Graph Theory. Quick primer; a graph database is a database that is based on graph theory. It consists of a set of objects, which can be a node or an edge.

- **Nodes** represent entities or instances such as people, businesses, accounts, or any other item to be tracked. They are roughly the equivalent of a record, relation, or row in a relational database, or a document in a document-store database.
- **Edges**, also termed graphs or relationships, are the lines that connect nodes to other nodes; representing the relationship between them. Meaningful patterns emerge when examining the connections and interconnections of nodes, properties and edges. The edges can either be directed or undirected. In an undirected graph, an edge connecting two nodes has a single meaning. In a directed graph, the edges connecting two different nodes have different meanings, depending on their direction. Edges are the key concept in graph databases, representing an abstraction that is not directly implemented in a relational model or a document-store model.
- **Properties** are information associated to nodes. For example, if Wikipedia were one of the nodes, it might be tied to properties such as website, reference material, or words that starts with the letter w, depending on which aspects of Wikipedia are relevant to a given database.

![graph-database](/img/GraphDatabase_PropertyGraph.png)
