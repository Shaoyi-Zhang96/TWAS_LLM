# Gene-Disease Association Analysis

## Overview
This project provides a comprehensive pipeline for analyzing gene-disease associations. The script extracts relevant information from PubMed, NCBI Gene database, and web search results to provide structured insights into biomedical relationships.

## Features
- **PubMed Article Retrieval**: Searches PubMed for relevant scientific literature.
- **Gene Information Lookup**: Retrieves gene details from NCBI Gene.
- **Web Search Integration**: Fetches additional context from general web searches.
- **Abstract Extraction**: Extracts abstracts from PubMed articles.
- **Automated Analysis**: Summarizes associations between genes, SNPs, and drugs with diseases.
- **Batch Processing**: Processes multiple gene-disease pairs from an input file.
- **Structured Output**: Generates CSV summaries for easy review.

## Requirements
The script requires the following Python packages:
- `requests`
- `beautifulsoup4`
- `lxml`
- `csv`
- `json`
- `openai`

Ensure these dependencies are installed before running the script:
```sh
pip install requests beautifulsoup4 lxml openai
```

## Setup
1. Clone this repository:
   ```sh
   git clone https://github.com/yourusername/gene-disease-analysis.git
   cd gene-disease-analysis
   ```
2. Replace `your api key` with your OpenAI API key in the script.
3. Run the script for batch processing:
   ```sh
   python script.py input_file.csv
   ```
   or for directory-based analysis:
   ```sh
   python script.py path/to/association/results/
   ```

## Input Format
The input file should be a txt tab-separated with the following structure:
```
Gene Disease
BRCA1 Breast Cancer
TP53 Lung Cancer
```

## Output
The results will be saved in the `gene_disease_results/` directory, with:
- **Individual reports**: Text files with analysis details for each gene-disease pair.
- **Summary CSV**: `association_summary.csv` containing structured insights.

## Example Output CSV
| Gene | Disease | Association | Confidence | Pathways | Functional Role | Cell Lines |
|------|---------|-------------|------------|-----------|-----------------|------------|
| BRCA1 | Breast Cancer | Yes | High | DNA Repair | Tumor Suppressor | MCF-7 |
| TP53 | Lung Cancer | Yes | Medium | Apoptosis | Cell Cycle Control | A549 |


## Contributors
- Shaoyi Zhang 
