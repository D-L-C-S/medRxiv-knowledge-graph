# 🧠 medRxiv Knowledge Graph

A powerful pipeline for constructing **knowledge graphs from medRxiv abstracts** using NLP and relation extraction techniques. Explore connections between biomedical entities such as drugs, diseases, proteins, and more.

---

## 📚 Project Overview

The pipeline extracts entities and relations from medRxiv abstracts and constructs a structured knowledge graph. The goal is to help researchers **visualize and explore relationships** in biomedical literature.

### Key Steps:

1. **Data Collection** – Download and clean medRxiv abstracts
2. **Entity Extraction** – Identify biomedical entities (drugs, diseases, proteins, etc.) using NLP
3. **Relation Extraction** – Identify candidate relationships between entities within sentences
4. **Graph Construction** – Convert entities and relations into a structured knowledge graph
5. **Visualization** – Explore the graph interactively with PyVis or export for analysis in Neo4j or CSV
6. **Export Results** – Save nodes and edges for downstream tasks

---

## 🗂️ Project Structure

```
medrxiv_knowledge_graph/
│
├── src/
│   ├── 1_data_collection.ipynb       # Collect raw abstracts from medRxiv
│   ├── 2_relation_extraction.ipynb   # Extract candidate relations between entities
│   ├── 3_graph_construction.ipynb    # Convert entities and relations into a graph
│   └── 4_export_results.ipynb        # Export nodes and edges for downstream tasks
│
├── data/
│   ├── abstracts_raw.json            # Collected abstracts
│   ├── entities_extracted.csv        # Extracted biomedical entities
│   └── relations.csv                 # Identified relationships between entities
│
├── models/
│   └── en_ner_bc5cdr_md-0.5.4.tar.gz  # Pre-trained NLP model for entity extraction
│
├── output/
│   ├── knowledge_graph_interactive.html  # Interactive HTML visualization of the knowledge graph
│   └── triples_output.csv               # CSV format of the knowledge graph (nodes and edges)
│
└── README.md                          # Project documentation
```

---

## ⚙️ Installation

### Step 1: Clone the repository

```bash
git clone https://github.com/yourusername/medrxiv-knowledge-graph.git
cd medrxiv-knowledge-graph
```

### Step 2: Create a Python virtual environment

```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
```

### Step 3: Install required packages

```bash
pip install -r requirements.txt
```

---

## 🚀 Usage

### 1. Data Collection

Run `1_data_collection.ipynb` to fetch abstracts from medRxiv and store them in `data/abstracts_raw.json`.

### 2. Relation Extraction

Run `2_relation_extraction.ipynb` to identify relations between entities in sentences. Outputs are saved in `data/relations.csv`.

### 3. Graph Construction

Run `3_graph_construction.ipynb` to convert entities and relations into a network graph.

### 4. Export Results

Run `4_export_results.ipynb` to save the graph nodes and edges for downstream analysis or Neo4j import.

---
