# Pubchem_Biomedical_Text_Mining_with_Python_-_NLP

This repository presents a biomedical text mining pipeline built in Python for extracting disease–chemical associations from PubMed abstracts using advanced NLP models (SciSpaCy).
It automatically fetches abstracts, identifies biomedical entities, filters valid compounds through PubChem, and visualizes drug–disease relationships using network graphs.

📚 Overview
Biomedical literature is a rich source of knowledge, but manually analyzing it is time-consuming. This script automates that process through:
* Automated data collection from PubMed using Biopython’s Entrez API
* Named Entity Recognition (NER) with SciSpaCy models (en_ner_bc5cdr_md and en_ner_bionlp13cg_md)
* Entity validation using PubChemPy
* Interactive visualization of drug–disease networks via PyVis

🚀 Key Functionalities
* Fetches and parses PubMed abstracts
* Extracts Diseases, Chemicals, and Proteins
* Filters chemical entities against PubChem database
* Counts and ranks frequent diseases and chemicals
* Generates an interactive drug–disease network graph


Installation & Setup
Clone the Repository
git clone https://github.com/yourusername/biomedical-text-mining.git
cd biomedical-text-mining

Install Dependencies
```python 
!pip install biopython scispacy pubchempy pyvis pandas networkx tqdm
```

Then install SciSpaCy biomedical models:
pip install https://s3-us-west-2.amazonaws.com/ai2-s2-scispacy/releases/v0.5.4/en_ner_bc5cdr_md-0.5.4.tar.gz
pip install https://s3-us-west-2.amazonaws.com/ai2-s2-scispacy/releases/v0.5.4/en_ner_bionlp13cg_md-0.5.4.tar.gz

🧠 Usage

Edit the search query in the script:

search_query = "(alzheimer) AND (alzheimer drug) NOT (Cancer)"


Run the script:

python exploring_biomedical_text_mining_from_pubmed_with_python_&_nlp.py


Outputs:

Prints top PubMed abstracts with title and year
Creates a dataframe (df_entities) containing all recognized entities
Displays a drug–disease interaction network in your browser

🧪 Example Output
PMID	Disease	Chemical	Year
12345678	Alzheimer’s disease	Donepezil	2024
23456789	Alzheimer’s disease	Memantine	2023

Network Visualization Example:
🧠 Alzheimer’s disease ↔ 💊 Donepezil ↔ 🧬 Protein interactions

📊 Visualization
An interactive HTML network (via PyVis) connects top 30 diseases and chemicals.
You can hover over nodes to see relationships and zoom in for details.
