# d3-force-troubleshooting

### Common problems I've had when building force-directed diagrams in d3.

* Nodes ignore force completely and appear in top left corner, overlapping.
 * You probably have duplicate links. You can have multiple links between nodes but they need unique names.
* Nodes are linked but ignore charge, so that all neighbor nodes 'collapse' and overlap with one another.
 * Do you have a custom `charge()` function? It might be broken.
