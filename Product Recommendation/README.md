## Product Recommendation
Here, I'm recommending products based on the category of the product purchased.

After preprocessing and identifying metrics like degree centrality, clustering coefficient, and similarity index, the recommendation of products is performed by:

1. Filtering Similar Products: An ego graph is constructed for a purchased product, and similar products are filtered based on a similarity threshold, creating a focused set of related products.

2. Rank and Display Top 5 Recommendations: These similar products are then ranked by their average rating and total reviews. The top 5 products are selected and their details (like title, sales rank, and ratings) are displayed as recommendations.
