# Surya Kiran Katragadda

**AI systems & backend engineer.** Alpharetta, GA · Kennesaw State University

I build backends that reason over messy real-world signal — audio, source code, faces,
natural language — and the pipelines that keep them fed. Most of what I ship runs locally,
on a schedule, or both.

---

## Selected work

### [flowstate](https://github.com/SuryaKiran434/flowstate) · Python, FastAPI, PostgreSQL
An emotional arc engine for music. Instead of static mood playlists, it asks *where are you,
and where do you want to go* — then builds a path between the two.

- **Custom audio ML** — 42-dimensional librosa feature vectors (MFCCs, chroma, spectral centroid, tempo) extracted via yt-dlp, classified with a RandomForest. Operates on raw audio, not lyrics, so it handles Telugu, Tamil, Hindi, Korean and English equally.
- **Graph path planning** — modified Dijkstra over a 12-node emotion graph, with edge weights that adapt per user from skip and completion signals.
- **Claude-powered mood parsing** — *"I'm burned out and want to decompress"* → structured source/target emotion pair.
- Airflow pipeline, MLflow tracking, Redis-backed OAuth2 PKCE, 428 passing tests.

### [code-intel](https://github.com/SuryaKiran434/code-intel) · Python, Milvus, tree-sitter
RAG over your own codebase. Indexes a Git repo with AST-aware chunking, embeds with
voyage-code-3, stores vectors in Milvus, and answers questions like *"how does the retry
logic work end-to-end?"*

- Multi-vector retrieval with query expansion and reranking
- Incremental re-indexing driven by git diffs — no full rebuilds
- Per-query telemetry: latency, retrieval scores, audit log
- Runs entirely local; code never leaves the machine except for embedding and LLM calls

### [face-recognition](https://github.com/SuryaKiran434/face-recognition) · Python, dlib
Real-time face recognition from a webcam or RTSP stream. 128-dimension encodings matched
by Euclidean distance, plus the offline tooling to build the encoding database.

### [taskmanagementtool](https://github.com/SuryaKiran434/taskmanagementtool) · Java, Spring Boot
Production-shaped REST backend: JWT auth with refresh tokens, role-based access control,
rate limiting, OpenAPI docs, and a full exception-handling layer.

### [movie-automation](https://github.com/SuryaKiran434/movie-automation) · Python
Watches Regal Cinemas for a movie on a target date and notifies me the moment showtimes
go live. Fast HTTPS path first, headless Chromium fallback when Cloudflare blocks it —
then deletes its own cron job once it fires.

### [folderlock-mac](https://github.com/SuryaKiran434/folderlock-mac) · Swift, SwiftUI
Right-click any file or folder in Finder and put a password on it. AES-256-GCM with
PBKDF2-SHA256 at 200k iterations, exposed through a native Finder Sync Extension.

---

## Stack

**Languages** — Python · Java · Swift · SQL · Shell · JavaScript

**AI/ML** — PyTorch-adjacent classical ML (scikit-learn), librosa, dlib, RAG pipelines,
vector search (Milvus), embedding + reranking models, Claude and GPT APIs

**Backend** — FastAPI · Spring Boot · PostgreSQL · Redis · Airflow · MLflow · Docker

---

## A note on frontends

I don't call myself a frontend engineer. But I care a lot about how the things I build
feel to use — lazy loading that hides the seams, animation that explains what just
happened, interfaces you understand without being told. When I build a UI, that's what
I'm chasing, and I'd rather work alongside someone who does it properly than pretend
I already do.

---

## Reach me

- Email — suryakiran.katragadda@gmail.com
- GitHub — you're already here
