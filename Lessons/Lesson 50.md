# 11/04/21: Graphs

| Word | Meaning |
| ---- | ------- |
| Node | Individual item |
| Edge | Connection between nodes |
| Neighbor | Another node that your node is connected to |
| Trail | Path that never hits the same node more than once |

## Graph Types
- Undirected graphs are connected both ways. Directed graphs are not, unless established in both ways
- All connections are weighted equally in an unweighted graph
- Graphs can be weakly/strongly connected depending on how easy it is to reach any node from another node in the graph
- In a connected graph, every node can be reached from every other node

![Visual](/Images/GraphTypes.png)

## Additional Notes
- Trees have roots because of their structure, but graphs have no top or order, and thus no root either
- From a data structure standpoint, trees are a variation of graphs
- **Trees are simplified graphs**, the main different is that trees have **a single distinct path** from any root to node, but in a graphs, multiple paths exist
- Iterative logic pairs well with linear data structures since these allows us to start at the parent and work down to the children. **Graphs work best with recursion because all the nodes are just neighbors**
- When we recurse in trees, we work down from the parent to the children and keep going down that way. This doesn't work for graphs because there is no progression, everything is just neighbors. You need to keep track of what nodes you already visited to ensure your algorithm isn't stuck in an eternal loop. **This can be done using a set.**