# dsc212-assignmentDSC-211 — Karate Club Community Detection (Spectral Modularity Method)

This repository contains an implementation of Newman’s spectral modularity maximization approach applied to Zachary’s Karate Club network. The method recursively divides the graph into smaller communities by examining the sign pattern of the dominant eigenvector of the modularity matrix. Through repeated bisection, the underlying faction structure of the club becomes visible.

Zachary’s dataset represents a friendship network among 34 members of a university karate club that famously split into two groups. Each vertex corresponds to a person, and edges indicate strong social interactions.

A) Community Detection Workflow

During execution, the notebook reports:

The largest eigenvalue at each recursive split

The resulting increase in modularity (ΔQ)

The partition of nodes into two subgroups

The final list of communities once no further positive eigenvalues remain

This provides a trace of how the network is broken down step-by-step.

B) Visual Outputs

The notebook produces several visual components:

A graph drawing for each iteration, showing how the network evolves as splits are performed

A final community visualization, with each group assigned a distinct color

Multiple centrality evolution plots, tracking how:

Degree centrality

Betweenness

Closeness

Clustering coefficient
behave across recursive splits

These help interpret how structural roles shift (or remain stable) throughout the algorithm.

C) Interpretation and Discussion

Some key findings:

Nodes 0 and 33 appear persistently influential according to several centrality measures

The resulting communities align closely with the historical split between the instructor’s faction and the club president’s faction

Centrality trends stay relatively consistent even as communities are subdivided, reflecting the stable core structure of the network

References

Newman, M. E. J. (2006). Modularity and community structure in networks. PNAS, 103(23), 8577–8582.

Zachary, W. W. (1977). An information flow model for conflict and fission in small groups.

Dependencies

This project uses:

networkx

numpy

scipy

matplotlib
