# 👗 VectorFashionSearch

A full-stack AI-powered fashion search engine that uses vector embeddings to find visually and semantically similar clothing items. Upload or describe a fashion item and get relevant matches ranked by similarity — not just keyword matches.

## ✨ Features

- **Semantic Search**: Find fashion items by natural language description (e.g. "floral summer dress with pockets")
- **Vector Similarity**: Uses embedding models to match items based on style, color, and category — beyond simple keyword search
- **Full-Stack Architecture**: Python FastAPI backend + modern frontend interface
- **REST API**: Clean API endpoints for integrating into other applications

## 🛠️ Tech Stack

**Backend**
- Python 3.10+
- FastAPI
- Vector database (e.g. Pinecone / Qdrant / Weaviate)
- Sentence Transformers / OpenAI embeddings

**Frontend**
- Node.js
- Modern JavaScript framework (Next.js / React)

## 📁 Project Structure

```
VectorFashionSearch/
├── backend/
│   └── app/          # FastAPI application, routes, embedding logic
├── frontend/         # Frontend UI
└── Readme.md
```

## 🚀 Getting Started

### Prerequisites

- Python 3.10+
- Node.js 18+
- A vector database account (Pinecone, Qdrant, or similar)
- API keys for your chosen embedding provider

### Backend Setup

```bash
cd backend/app
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
```

Create a `.env` file in `backend/app/`:

```env
VECTOR_DB_API_KEY=your_key_here
VECTOR_DB_ENVIRONMENT=your_env
EMBEDDING_API_KEY=your_key_here
```

Start the backend:

```bash
uvicorn main:app --reload
```

The API will be available at `http://localhost:8000`. Interactive docs at `http://localhost:8000/docs`.

### Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

The frontend will be available at `http://localhost:3000`.

## 🔍 How It Works

1. Fashion items are embedded into high-dimensional vectors using a language/vision model
2. Vectors are stored in a vector database with associated metadata (category, color, brand, etc.)
3. A user query (text or image) is embedded using the same model
4. The system performs approximate nearest-neighbor search to find the most similar items
5. Results are ranked by cosine similarity and returned to the frontend

## 📡 API Reference

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/search` | Search by text query |
| `POST` | `/search/image` | Search by image upload |
| `GET`  | `/items/{id}` | Get item details |
| `POST` | `/items` | Index a new item |

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you'd like to change.

## 📝 License

MIT
