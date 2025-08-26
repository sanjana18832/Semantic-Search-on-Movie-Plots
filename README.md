## **Author**: Sanjana Sori (221010241, ECE)

# 🎬 Semantic Search on Movie Plots  

This repository is based on the [Semantic Search on Movie Plots project](https://github.com/sanjana18832/Semantic-Search-on-Movie-Plots).  
It contains my solution for **Assignment-1: Semantic Search on Movie Plots** using **SentenceTransformers** (`all-MiniLM-L6-v2`).  

The system encodes movie plots into embeddings and retrieves the most semantically relevant movies for a given query using cosine similarity.  

---

## ✅ What I Did
- Built a **semantic search engine** in `movie_search.py` using **all-MiniLM-L6-v2** from SentenceTransformers  
- Encoded movie plots into embeddings and computed **cosine similarity** (normalized to 0–1) for retrieval  
- Added a **command-line interface (CLI)** to run queries with `--query` and `--top-n` options  
- Implemented **unit tests** in `tests/test_movie_search.py` to validate:
  - Output format & DataFrame columns  
  - Correct number of results (`top_n`)  
  - Similarity range (0–1)  
  - Relevance ranking  
- Created a **sample dataset** (`movies.csv`) with movie titles and plots for quick testing  
- Documented setup, usage, and troubleshooting in this `README.md`  

---

## 📂 Repository Structure
- `movie_search.py` → Module implementing semantic search  
- `movies.csv` → Tiny sample dataset (title, plot)  
- `tests/test_movie_search.py` → Unit tests for `search_movies`  
- `requirements.txt` → Project dependencies  
- `README.md` → Documentation  

---

## 🖥️ Prerequisites
- Python **3.9+**  
- Git  

---

## 🔗 Clone the Repository
```bash
git clone https://github.com/sanjana18832/Semantic-Search-on-Movie-Plots.git
cd Semantic-Search-on-Movie-Plots
```
⚙️ Create and Activate Virtual Environment
Choose the command that matches your shell/OS.

Linux/macOS (Bash/Zsh):
```bash
python -m venv venv
source venv/bin/activate
```
Windows (PowerShell):
```bash
python -m venv venv
venv\Scripts\Activate.ps1
```
📦 Install Dependencies
```bash
pip install -r requirements.txt
```
🚀 How to Run
Run a query directly from the terminal using the CLI:
```bash
python movie_search.py --query "spy thriller in Paris" --top-n 3
```
This prints a concise table with title and similarity.

🧪 Run Unit Tests
```bash
python -m unittest tests/test_movie_search.py -v
```
📊 Notes
Model used: sentence-transformers/all-MiniLM-L6-v2

Similarity metric: Cosine similarity (scaled to 0–1)

📝 Example
```bash
python movie_search.py --query "spy thriller in Paris" --top-n 2
```
Expected: The movie "Spy Movie" ranks at the top.
