For identifying and analyzing centrality metrics of the Amazon co-purchasing network, only the DVD subgroup - 19,828 products is considered as the full product network is very large - 548,552 products which is computationally costly.

Centrality metrics for the DVD category:

1. Degree Centrality
Degree Centrality is a measure of the importance of a node in a network. It is calculated as the number of edges connected to a node (degree) divided by the maximum number of edges that could potentially connect it to other nodes (n-1, where n is the total number of nodes in the network).
From this metric, we can identify the most popular node - DVD in the network.

2. Betweenness Centrality
Betweenness Centrality is a measure of a node's importance in a graph. It measures how many shortest paths travel through a node, which indicates how important it is in the network.
From this metric, we can find the product which is bought frequently with other products.

4. Closeness Centrality
Closeness centrality is a measure of how close a node is to all other nodes in a network. It is calculated as the inverse of the sum of the shortest path distances from that node to all other nodes in the network.
From this metric, we can identify the most co-purchased items.

5. Eigenvector centrality
Eigenvector Centrality is a measure of the importance of a node in a network. It is based on the idea that a node is important if it is connected to other important nodes. The significance of a node is determined by the significance of its neighbors.

There are different categories like horror, comedy, documentary, kids, drama, anime, action, mystery, music, and science, and also, some DVDs belong to multiple categories. Degree, betweenness, and closeness centrality are calculated after splitting the data according to each category.

