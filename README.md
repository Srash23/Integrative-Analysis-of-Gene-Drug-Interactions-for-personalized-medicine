# Drug-Gene Interaction Network Analysis

This repository explores the relationships between drugs and genes using real-world interaction data. The analysis pipeline includes descriptive statistics, network graph modeling, distribution analysis, hierarchical clustering, and PCA to identify key drug and gene players.

## Project Overview
This project aims to:
- Identify top drugs and genes by interaction frequency
- Construct a bipartite drug-gene interaction network
- Analyze centrality to identify key influencers
- Visualize interaction distributions
- Perform clustering and dimensionality reduction

## Dataset Description
| Column        | Description                           |
|---------------|---------------------------------------|
| `#Drug`       | Drug name or ID (e.g., DB00157)       |
| `Gene`        | Associated gene/protein ID            |

## Analytical Workflow

### **Descriptive Statistics & Bar Plots**
- Top 10 drugs and genes by frequency
- Drug-gene relationships visualized using `seaborn`

### **Centrality Analysis**
- Construct drug-gene bipartite graph using `NetworkX`
- Compute degree centrality to find hubs in the network

### **Network Graph**
- Visualize a subgraph of top 50 nodes (drugs + genes)
- Spring layout for intuitive relationship clustering

### **Distribution Analysis**
- Count interactions per drug and gene
- Plot histograms and KDEs for interaction distributions
- Categorize into Low, Medium, High bins for both

### **Clustering & PCA**
- Create a binary interaction matrix
- Perform hierarchical clustering (`scipy`) with dendrogram
- Run PCA and visualize components with `matplotlib`

## Required Libraries
```bash
pip install pandas seaborn matplotlib networkx scikit-learn scipy
```
## Key Insights
- Identifies top candidate genes targeted by multiple drugs
- Reveals highly promiscuous drugs (interacting with many genes)
- Provides intuitive visual network structure
- Highlights gene clusters and outliers via PCA and dendrograms

## License
MIT License – open to use and contribution.
