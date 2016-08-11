# d3-force-troubleshooting

### Common problems I've had when building force-directed diagrams in d3.

* Nodes ignore force completely and appear in top left corner, overlapping.
 * You may have duplicate links. You can have multiple links between nodes but they need unique names.
 * It may also be a problem with the link ids.
 * Did you start the force simulation?
 * This also happens when the nodes are not updated correctly. (I had `nodeEnter.merge(node)` instead of `node = nodeEnter.merge(node)`)
* Nodes are linked but ignore charge, so that all neighbor nodes 'collapse' and overlap with one another.
 * Do you have a custom `charge()` function? It might be broken.
* Nodes are arranged and linked together correctly but links don't show up.
 * Are the links formatted correctly (e.g. in CSS)? (and does their class match and all that)
 * 
