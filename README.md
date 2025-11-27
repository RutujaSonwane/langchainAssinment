# LangChain Character Extractor – Assignment 

A complete RAG (Retrieval-Augmented Generation) system that extracts structured character information from stories using **MistralAI** as required by the assignment.

**All requirements satisfied**  
Uses **MistralAI** for embeddings & LLM  
Local Chroma vector database  
Perfect JSON output  
Handles edge cases  
Clean code, no secrets leaked

### How to Run (Step-by-Step Demo)

1. **Get your free Mistral API key**  
   https://console.mistral.ai → API Keys → Create new key

2. **Create `.env` file** in this folder:
   ```env
   MISTRAL_API_KEY=sk-your-real-key-here

3. Install dependencies
pip install -r requirements.txt

4. Run the project 
Step 1: Build the vector database (run only once)
```
python main.py compute-embeddings
```
Step 2: Get character info
```
python main.py get-character-info "Jon Snow"
```

### Expected Output (Exactly as Assignment Requires)
{

  "name": "Jon Snow",

  "storyTitle": "A Song of Ice and Fire",
  
  "summary": "Jon Snow is a brave and honorable 
  
  leader who serves as the Lord Commander of the 
  
  Night's Watch and later unites the Free Folk and 
  
  Westeros against the threat of the White Walkers.",
  
  "relations": [
    { "name": "Arya Stark", "relation": "Sister" },
  
    { "name": "Eddard Stark", "relation": "Father" }
  ],
  
  "characterType": "Protagonist"
}
