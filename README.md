# 🎧 Vibe Matcher — AI-Powered Fashion Recommender

An AI-driven prototype that matches user **vibe queries** (like “energetic urban chic”) to the most relevant fashion items using **text embeddings** and **cosine similarity**.  
The system captures *mood, style, and context* beyond literal keywords — enabling a more human, emotion-based recommendation experience.

---

## 🧠 Project Overview

This notebook simulates a **mini recommendation system** that:
1. Takes a **vibe query** as input (e.g., "cozy winter look")
2. Embeds both product descriptions and queries into semantic vectors
3. Computes **cosine similarity** to find top-3 matching fashion items
4. Outputs the matches with similarity scores and latency metrics

If OpenAI API credits are unavailable, the notebook automatically switches to a **local SentenceTransformer model (MiniLM)** for embeddings — ensuring full offline functionality.

---

## 🧱 Tech Stack

- **Python 3.10+**
- **Pandas** – data handling  
- **Scikit-learn** – cosine similarity computation  
- **Matplotlib** – latency visualization  
- **OpenAI API (text-embedding-ada-002)** – optional embeddings  
- **SentenceTransformers (all-MiniLM-L6-v2)** – free fallback embeddings

---

## ⚙️ Workflow

| Step | Description | Tools |
|------|--------------|-------|
| **1. Data Prep** | Created 10 mock fashion products with names, descriptions, and vibe tags | Pandas |
| **2. Embeddings** | Generated vector embeddings via OpenAI API or local MiniLM model | OpenAI / SentenceTransformers |
| **3. Vector Search** | Computed cosine similarity between query & product embeddings | Scikit-learn |
| **4. Evaluation** | Logged latency, plotted performance, rated similarity scores | Matplotlib |
| **5. Reflection** | Documented improvements and scalability considerations | Markdown |

---

## 🧪 Sample Queries & Results

| Query | Top Match | Example Score |
|--------|------------|---------------|
| "energetic urban chic" | Streetwear Hoodie | 0.86 |
| "soft and cozy winter outfit" | Cozy Knit Sweater | 0.82 |
| "luxurious evening style" | Silk Evening Gown | 0.90 |

---

## 📈 Evaluation Metrics

- **Cosine Similarity > 0.7** → counted as a “Good” match  
- **Latency Plot** → shows time taken per query  
- **Fallback Mechanism** → ensures uninterrupted execution even without API credits  

---

## 💡 Reflection & Next Steps

- Implement **Pinecone** or **FAISS** for scalable vector search.  
- Add **hybrid scoring** combining vibes + embeddings.  
- Cache embeddings to reduce latency.  
- Expand dataset to include accessories and mood-specific subcategories.  
- Deploy via Streamlit for real-time vibe-based fashion recommendations.

---

## 🌟 Why AI at Nexora?

> At Nexora, I see AI not as an add-on, but as the creative core that transforms data into intuition.  
> The “Vibe Matcher” prototype reflects that belief — blending human understanding of mood and context with the precision of vector embeddings.  
> I’m inspired by Nexora’s mission to use AI for *personalized, meaningful experiences* that make technology feel human.

---

## 👩‍💻 Author

**Paridhi Sharma**  
B.Tech (IGDTUW) | Data Science & AI Enthusiast  
📍 India  
🔗 [LinkedIn](https://www.linkedin.com/in/paridhi-sharma-013721207/)  
📧 Contact: [via LinkedIn or GitHub Issues]

---

## 📂 Repository Structure
Vibe_Matcher_Recommender/
│
├── Vibe_Matcher_Recommender.ipynb # Main Colab notebook
├── README.md # Project documentation
└── requirements.txt # (Optional) Dependencies for local run


---

## 🚀 How to Run

### **In Google Colab**
1. Open [Google Colab[]](https://colab.research.google.com/drive/1rRXSDriUU-ZxXwsRkyG8dC5bogDq-CxQ)
2. Upload `Vibe_Matcher_Recommender.ipynb`
3. (Optional) Add your OpenAI API key in the first cell
4. Run all cells → view vibe matches + latency plots

### **Locally**
```bash
git clone https://github.com/theparidhisharma/Vibe_Matcher_Recommender.git
cd Vibe_Matcher_Recommender
pip install -r requirements.txt
jupyter notebook Vibe_Matcher_Recommender.ipynb
