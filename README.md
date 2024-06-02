# One Million Financial News Processing


## Notebook 1: Filter Out the News in A-list Company -- Similarity

### Objective 
This notebook focuses on Named Entity Recognition (NER) and similarity analysis for financial news.
<img width="683" alt="截屏2024-06-02 下午3 50 10" src="https://github.com/Fayeww/NLP/assets/147254244/85d5f15d-0328-4e08-85b7-9275b423d74a">

### Steps

1. **Data Preprocessing:** Clean and preprocess news content for analysis.
2. **NER with LAC:** Implement Named Entity Recognition using Baidu's LAC (Lexical Analysis of Chinese) tool.
3. **Embedding with BERT:** Utilize BERT-based embeddings to represent A-share company names.
4. **Similarity Analysis:** Assess the similarity between news content and A-share companies.
5. **Matching A-share Companies:** Identify A-share companies based on similarity scores.

**Files to Read:**
1. `News.xlsx` - News data file.
2. `A_share_list.json` - A-share company list.
3. `NER.csv` - NER result file.



## Notebook 2: Brute Force Matching & Sentiment Analysis

### Objective
This notebook performs brute force matching and sentiment analysis on financial news.

### Steps

1. **Data Loading:** Load processed data from the NER & Similarity notebook.
2. **Data Preprocessing:** Clean and preprocess news content for sentiment analysis.
3. **Explicit Company Matching:** Match explicit company names in news content.
4. **Labeling:** Apply sentiment labels to each news article.
5. **Analysis:** Explore sentiment distribution and save results.

**Files to Read:**
1. `Explicit_Company_*.csv` - Merged data files.
2. `processed_data.csv` - Keyword matching result file.

## Notebook 3: Graph Construction

### Objective
This notebook constructs a knowledge graph using Neo4j for financial relationships.

### Steps

1. **Neo4j Connection:** Establish a connection to the Neo4j database.
2. **Graph Building:** Create relationships based on various financial interactions (e.g., cooperate, compete).

**Files to Read:**
1. `hidy.relationships.supply.csv`, `hidy.relationships.same_industry.csv`, `hidy.relationships.invest.csv`, `hidy.relationships.dispute.csv`, `hidy.relationships.cooperate.csv`, `hidy.relationships.compete.csv` - Information files for relationship edges in Neo4j.
## Notebook 4: Find the Implicit Impact of Each News According to the Knowledge Graph

### Objective
This notebook analyzes financial relationships extracted from the knowledge graph.

### Steps

1. **Data Transformation:** Convert company names to IDs for graph analysis.
2. **Graph Querying:** Query graph relationships for implicit positive and negative company interactions.


**Files to Read:**
1. `fv.csv` - Sentiment analysis result file.
2. `A_share_list.json` - A-share company list.
3. `hidy.nodes.company.csv` - Information file for company nodes in Neo4j.
4. `hidy.relationships.supply.csv`, `hidy.relationships.same_industry.csv`, `hidy.relationships.invest.csv`, `hidy.relationships.dispute.csv`, `hidy.relationships.cooperate.csv`, `hidy.relationships.compete.csv` - Information files for relationship edges in Neo4j.

## Notebooks' Dependencies

- Python Libraries: pandas, numpy, torch, transformers, google.colab, LAC, torch.nn.functional, heapq, bixin, neo4j, csv
- External Files: News.xlsx, A_share_list.json, checkpoint files, explicit company CSVs, financial relationship CSVs.

