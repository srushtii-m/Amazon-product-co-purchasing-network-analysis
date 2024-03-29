# Amazon Product Co-Purchasing Network Analysis
This project presents a system for analyzing and recommending Amazon products, leveraging a dataset of over half a million reviews and metadata. It utilizes network analysis to understand product relationships, focusing on centrality metrics within the DVD category. The system includes regression models to predict product sales ranks and uses ego graph-based methods for product recommendation, ranking items based on user reviews and ratings. Although it explores community detection concepts, computational limitations restrict their implementation. It gives data-driven insights into customer purchasing patterns and product positioning in the Amazon marketplace.

![image](https://github.com/srushtii-m/Amazon-product-co-purchasing-network-analysis/assets/146901085/459b1225-6cc9-4094-aecf-f94bbea83779)

## Motivation
The motivation behind this project was to analyze the vast and complex dataset of Amazon and understand the nuances of consumer behavior and product relationships. The project provided an opportunity to apply network analysis techniques in a real-world context and leverage network theory and data analytics to create a graph-based recommendation system based on user behavior.

## Data
[Stanford Large Network Dataset Collection](https://snap.stanford.edu/data/amazon-meta.html)

The dataset includes 548,552 different product reviews and product metadata (Books, music CDs, DVDs, and VHS video tapes).

## Key Components of this Project
* [Amazon Co-Purchase Network Analysis](https://github.com/srushtii-m/Amazon-product-co-purchasing-network-analysis/tree/1b1c0533d2989fe47f43e3684965f41426e173d6/Network%20Analysis)
* [Analysis of Network Centrality Metrics](https://github.com/srushtii-m/Amazon-product-co-purchasing-network-analysis/tree/1b1c0533d2989fe47f43e3684965f41426e173d6/Centrality%20Metrics)
* [Product Recommendation](https://github.com/srushtii-m/Amazon-product-co-purchasing-network-analysis/tree/1b1c0533d2989fe47f43e3684965f41426e173d6/Product%20Recommendation)

## Conclusion
* The popularity of products can be effectively gauged using metrics like degree centrality and clustering coefficient and a priority queue can be established for marketing, sales, and advertising efforts.
* Could identify influential products within the amazon's product network through different centrality metrics
* Implemented Regression models to predict sales rank but it gave low scores implying that, in network scenarios, standard machine learning methods based on probability density estimation tend to underperform.
* Could build a graph-based product recommendation system, where purchase history, product similarity, and customer feedback are all taken into account to suggest relevant products to customers effectively.
* The findings from this project could inform strategic decisions for businesses operating in the e-commerce domain.
