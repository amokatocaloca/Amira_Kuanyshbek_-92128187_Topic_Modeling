README for Text Analysis Script

Overview
This script is designed for processing and analyzing large collections of text data from scientific literature. The goal is to extract, categorize, and visualize significant topics within the corpus using advanced natural language processing (NLP) techniques.

Prerequisites
- Python 3.x
- Libraries: `sentence_transformers`, `hdbscan`, `dask`, `pandas`, `numpy`, `seaborn`, `matplotlib`, `umap-learn`, `nltk`, `scikit-learn`
- Install the required libraries using `pip install sentence_transformers hdbscan`.

Features
- Text preprocessing with normalization, tokenization, and lemmatization.
- Vectorization of text using CountVectorizer and TfidfVectorizer.
- Dimensionality reduction using UMAP for better clustering.
- Clustering with HDBSCAN to identify topic groups.
- Visualization of clusters with Seaborn and Matplotlib.

Usage
1. Ensure all dependencies are installed.
2. Load your dataset containing scientific literature. The script is currently set up to work with JSON files containing titles, abstracts, and other metadata.
3. Preprocess the titles and abstracts to prepare for vectorization.
4. Vectorize the processed text to create normalized feature matrices.
5. Reduce dimensionality with UMAP and perform clustering with HDBSCAN.
6. Visualize the results using a 2D scatter plot to identify distinct clusters.
7. Export the clustered data to a CSV file for further analysis or visualization.

Data Structure
- The dataset should be a collection of documents with fields for `title`, `abstract`, and `categories`.
- The script processes these fields to extract topics and categorizes them into clusters.

Output
- A CSV file containing the clustered documents with additional columns for the cluster labels and topics.
- A 2D scatter plot visualizing the distribution of documents across the clusters.

Post-Processing
- The script outputs a high-level overview of topics across clusters. For detailed analysis, use the CSV output to explore topics within each cluster.
- The second part of the script requires the path to the clustered data CSV file to perform further analysis and visualization.

Note
- e63bd3159d should be executed first
- The script may require adjustments to the file paths, parameters for vectorization, dimensionality reduction, and clustering to suit the specific dataset and analysis needs.
- It is advised to review and adjust the hyperparameters for UMAP and HDBSCAN based on the dataset size and computational resources.

Remember to download the filtered and clustered data from the first part of the script before proceeding to the second notebook. Adjust the file paths in the second notebook to point to your downloaded data.
