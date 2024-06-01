# Project Documentation

## Notebook 1: NER & Similarity (Task1 Q1)

### Objective 
This notebook focuses on Named Entity Recognition (NER) and similarity analysis for financial news.

### Steps

1. **Data Loading:** Load financial news data and A-share company list.
2. **Data Preprocessing:** Clean and preprocess news content for analysis.
3. **NER with LAC:** Implement Named Entity Recognition using Baidu's LAC (Lexical Analysis of Chinese) tool.
4. **Embedding with BERT:** Utilize BERT-based embeddings to represent A-share company names.
5. **Similarity Analysis:** Assess the similarity between news content and A-share companies.
6. **Matching A-share Companies:** Identify A-share companies based on similarity scores.
7. **Data Persistence:** Save processed data to CSV for further use.

**Files to Read:**
1. `News.xlsx` - News data file.
2. `A_share_list.json` - A-share company list.
3. `NER.csv` - NER result file.



## Notebook 2: Brute Force & Sentiment Analysis (Task1 Q1 & Q2)

### Objective
This notebook performs brute force matching and sentiment analysis on financial news.

### Steps

1. **Data Loading:** Load processed data from the NER & Similarity notebook.
2. **Data Merging:** Combine data from multiple CSV files for comprehensive analysis.
3. **Data Preprocessing:** Clean and preprocess news content for sentiment analysis.
4. **Explicit Company Matching:** Match explicit company names in news content.
5. **Labeling:** Apply sentiment labels to each news article.
6. **Analysis:** Explore sentiment distribution and save results.

**Files to Read:**
1. `Explicit_Company_*.csv` - Merged data files.
2. `processed_data.csv` - Keyword matching result file.

## Notebook 3: Graph Construction (Task2 Q3)

### Objective
This notebook constructs a knowledge graph using Neo4j for financial relationships.

### Steps

1. **Neo4j Connection:** Establish a connection to the Neo4j database.
2. **Graph Building:** Create relationships based on various financial interactions (e.g., cooperate, compete).
3. **Checkpointing:** Save checkpoints during the graph-building process.

**Files to Read:**
1. `hidy.relationships.supply.csv`, `hidy.relationships.same_industry.csv`, `hidy.relationships.invest.csv`, `hidy.relationships.dispute.csv`, `hidy.relationships.cooperate.csv`, `hidy.relationships.compete.csv` - Information files for relationship edges in Neo4j.
## Notebook 4: Financial Analysis (Task2 Q4)

### Objective
This notebook analyzes financial relationships extracted from the knowledge graph.

### Steps

1. **Data Loading:** Load processed data from the Sentiment Analysis notebook.
2. **Data Transformation:** Convert company names to IDs for graph analysis.
3. **Graph Querying:** Query graph relationships for implicit positive and negative company interactions.
4. **Data Cleanup:** Format results for further analysis.
5. **Data Export:** Save results for external use.

**Files to Read:**
1. `fv.csv` - Sentiment analysis result file.
2. `A_share_list.json` - A-share company list.
3. `hidy.nodes.company.csv` - Information file for company nodes in Neo4j.
4. `hidy.relationships.supply.csv`, `hidy.relationships.same_industry.csv`, `hidy.relationships.invest.csv`, `hidy.relationships.dispute.csv`, `hidy.relationships.cooperate.csv`, `hidy.relationships.compete.csv` - Information files for relationship edges in Neo4j.

## Notebooks' Dependencies

- Python Libraries: pandas, numpy, torch, transformers, google.colab, LAC, torch.nn.functional, heapq, bixin, neo4j, csv
- External Files: News.xlsx, A_share_list.json, checkpoint files, explicit company CSVs, financial relationship CSVs.

Feel free to reach out if you have any questions or need further clarification.
