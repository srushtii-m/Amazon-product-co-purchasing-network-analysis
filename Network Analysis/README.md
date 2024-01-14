## Analyzing Amazon Product Network

### Data Preprocessing
* Amazon product data is extracted from a raw text file and structured into a dictionary. Each product's ID, title, category, sales rank, related products, and review details are stored under its ASIN (Amazon Standard Identification Number).
* Product attributes like ID, title, group (category), sales rank, similar products (related products), and reviews are extracted from the text.
* The startswith method is used to identify lines containing specific attributes.
* For categories, a more complex process is used. It involves reading multiple lines, removing digits and punctuation, excluding common English stopwords, and applying stemming to the words.
Numeric values (ranking, review_count, and average_rating) are converted from strings to appropriate numeric types.
* Textual data is cleaned and formatted. For example, the title is stripped of extra spaces, and category names are processed to remove unnecessary characters and words.

### Similarity between two connected nodes
* For each product ID, a node is created, and similar products are also added as nodes. An edge is created between each product and its connected (similar) products.
* A similarity score is calculated based on these categories using the Jaccard index to quantify the relationship between the products and used as the weight of the edge in the graph.
* This graph can be used for various analyses like finding clusters of similar products, identifying key products (nodes) based on their connections, or even recommending similar products based on the graph's structure.

### Dimensionality Reduction
Due to computational limitations and to identify significant products, the top 50 eigenvalues, and eigenvectors were used to perform k-means clustering.
![image](https://github.com/srushtii-m/Amazon-product-co-purchasing-network-analysis/assets/146901085/61110c4a-7537-4393-b83c-d4a3f645eae2)

### Regression Models
To understand product relationships better, key network analysis metrics like degree centrality, ego graph, and clustering coefficient for each product were incorporated into the dataset.
![image](https://github.com/srushtii-m/Amazon-product-co-purchasing-network-analysis/assets/146901085/6552af17-77a0-4e28-8260-a776648bcf73)

* Degree centrality: The data shows that only a small fraction of nodes possess a degree centrality greater than zero, indicating that these nodes are more central compared to the majority of products. These specific products should be the focus of the marketing department as they hold the potential to act as influential or catalyst products. The associations they have with other products are likely due to the others being accessories or essential for the main product's functionality.

* Clustering coefficient: Numerous items in the Amazon co-purchase dataset exhibit a clustering coefficient exceeding 0.2, as indicated by the curve's area, suggesting that roughly one-sixth of the products fall into this category. Based on their clustering coefficients, a priority queue can be established for marketing, sales, and advertising efforts. This approach is crucial for enhancing engagement through non-organic growth strategies.

* For regression, salesrank, total reviews, average rating, degree centrality, and clustering coefficient features are used. 
* The regression model is designed to forecast the Sales Rank, where a lower rank indicates higher sales. Consequently, the model's coefficients are anticipated to be negative, reflecting that an increase in the feature values should correspond to a lower-rank prediction.

* To enhance the model's effectiveness, regularization techniques such as Lasso and Ridge Regression were utilized to adjust the feature set. 
The experiment demonstrated that as the regularization term's value is increased, there is a corresponding decrease in the R^2 value. Higher levels of regularization may lead to a model that is less capable of capturing the variance in the dataset, potentially due to over-penalization of the model's coefficients.

### Community Detection
* Community detection can be used as a feature to improve the accuracy of predictive models. For example, in recommendation systems, knowing which community a user belongs to can help in making more accurate recommendations. 
* Commonly, algorithms like the Girvan Newman Algorithm are employed for this purpose. Nevertheless, the implementation of such algorithms was impractical for this dataset, primarily because of their extensive time complexity, which is a function of the number of edges (E) and nodes (N) in the network, leading to computational constraints that hindered this approach.
