#  PlantGPT: AI-Powered Semantic Gene Search for Rice

> An intelligent semantic search engine for rice (Oryza sativa) genes using Sentence Transformers and FAISS.

![Python](https://img.shields.io/badge/Python-3.10+-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green)
![FAISS](https://img.shields.io/badge/FAISS-Semantic%20Search-orange)
![SentenceTransformers](https://img.shields.io/badge/SentenceTransformers-Embeddings-red)
![License](https://img.shields.io/badge/License-MIT-lightgrey)



##  Overview

PlantGPT is a Retrieval-Based AI system designed to perform **semantic search over rice genomic data**.

Instead of relying on exact keyword matching, PlantGPT understands the **meaning** of biological queries using transformer-based sentence embeddings and retrieves biologically relevant genes.

This project integrates:

- Rice genome annotation (GFF3)
- Protein sequences (FASTA)
- Gene Ontology (GO) annotations
- Sentence Transformers
- FAISS vector search

to create an AI-powered search engine capable of answering natural language biological queries.



##  Motivation

Modern genomic databases primarily support keyword-based searches.

For example,

```
photosystem II protein
```

may fail to retrieve genes annotated as

```
photosynthetic electron transport
```

even though both describe closely related biological processes.

PlantGPT addresses this limitation using **semantic similarity**, allowing researchers to search using natural language.


# Workflow

```
             GFF3
               │
               ▼
      Gene Coordinates

Protein FASTA ───────┐
                     │
GO Annotation ───────┤
                     ▼
        Integrated Rice Database
                     │
                     ▼
           Search_Text Creation
                     │
                     ▼
     Sentence Transformer Encoder
                     │
                     ▼
        384-Dimensional Embeddings
                     │
                     ▼
               FAISS Index
                     │
                     ▼
        Natural Language Query
                     │
                     ▼
      Top Matching Rice Genes
```


#  Project Structure

```
PlantGPT/

│
├── data/
│   ├── rice_gene_database.csv
│   ├── rice_annotations.txt
│   ├── Oryza_sativa.IRGSP-1.0.63.gff3
│   └── Oryza_sativa.IRGSP-1.0.pep.all.fa
│
├── notebook/
│   ├── 01_build_database.ipynb
│   └── 02_semantic_search.ipynb
│
├── embeddings/
│
├── README.md
│
└── requirements.txt
```



#  Features

- Integrates multiple biological data sources
- Cleans and preprocesses genome annotations
- Generates natural-language gene descriptions
- Converts gene descriptions into embeddings
- Builds a FAISS similarity index
- Performs semantic gene retrieval
- Supports natural language queries



#  Technologies Used

 Programming - Python 
 Data Processing -Pandas, NumPy 
 AI - Sentence Transformers 
 Embeddings - all-MiniLM-L6-v2 
 Vector Search - FAISS 
 Version Control - Git, GitHub 


#  Biological Data

PlantGPT combines information from:

- Gene IDs
- Transcript IDs
- Chromosome coordinates
- Protein sequences
- Protein lengths
- Gene Ontology (GO)
- Functional descriptions
- Gene biotypes



#  How Semantic Search Works

Instead of comparing words,

```
Query

↓

Embedding

↓

FAISS Similarity Search

↓

Nearest Gene Embeddings

↓

Relevant Genes
```

PlantGPT compares the **meaning** of biological descriptions.

---

#  Example Query

```text
Ask PlantGPT:

photosynthesis
```

Example Output

| Gene ID | GO Terms |
|----------|----------|
| Os01g0869800 | photosynthesis |
| Os04g0523000 | photosystem II |
| Os07g0105600 | chloroplast |


#  Dataset Statistics

| Feature | Value |
|----------|------:|
| Protein-coding genes | 35,806 |
| Total rice genes | 37,864 |
| GO annotations | ~21,500 |
| Embedding size | 384 |
| Embedding model | all-MiniLM-L6-v2 |

---

#  Future Improvements

- Streamlit web interface
- Retrieval-Augmented Generation (RAG)
- Multi-species support
- ChromaDB integration
- Local LLM integration
- Gene summary generation
- Protein similarity search


#  Learning Outcomes

This project demonstrates:

- Bioinformatics data integration
- Python for genomics
- Data preprocessing
- Semantic embeddings
- Vector databases
- AI-powered information retrieval
- Retrieval-Augmented AI concepts



#  Author

**Lavanya Raina**

M.Tech Computational Biology


