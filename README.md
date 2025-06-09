## Analysis of Illegal Advertisements.
The project aims to analyze a set of given advertisements related to health supplements, cosmetics, medicines, and medical devices to determine whether they violate relevant advertising regulations. We designed a Retrieval-Augmented Generation (RAG) system that embeds reference cases of illegal advertisements into a vector database. This setup allows the system to retrieve the most relevant cases for a given advertisement and evaluate its legality based on regulatory context and precedent cases. The embedding model and the language model are accessed via OpenAI API keys, enabling scalable and secure model inference.

## Models
- Embedding model (OpenAI): `text-embedding-3-large`
- Language model (OpenAI): `gpt-4.1`

## File Structure
```
AI_final_project/
├── Analysis_of_Illegal_Advertisements.ipynb       # Main Jupyter notebook for building the RAG system
├── cases.json                                     # JSON file containing labeled reference cases of illegal advertisements
├── formatted_cases.txt                            # Formetted text version of the cases, preprocessed for embedding
├── final_project_query.csv                        # CSV file with input queries or ad samples to be analyzed
├── requirements.txt                               # Python dependencies required to run the project
└── 法規及案例 Vector Stores/                       # Directory containing JSON files of legal rules and reference phrases
    ├── 13項保健功效及不適當功效延申例句之參考.json
    ├── 中藥成藥不適當共通性廣告詞句.json
    ...
```

## How to Use
### 1. Install the required packages listed in `requirements.txt`.
### 2. Set the api key by the following command
```bash
export OPENAI_API_KEY = <your api key>
```
### 3. Run `Analysis_of_Illegal_Advertisements.ipynb`
### 4. Results will be saved in `final_project_results.csv` following the format:
```csv
ID,Result
0,1        # legal
1,1        # legal
2,0        # illegal
...
```
