<h1 align="center">Kelvin Mendoza</h1>
<h3 align="center">Backend Software Engineer · Python & AI/LLM Integration</h3>

---

### About

Backend engineer working in Python: REST APIs, data modeling, automation, and
LLM integration. I design, build, and operate the software behind two content
platforms I own — end to end, from schema to deployment.

I launched **RiptoForex** in 2018 and **TedigoUnaVaina** in 2021 on WordPress.
Both went offline when the original hosting lapsed. In December 2025 I started
rebuilding RiptoForex on a custom Python backend I architected myself, and did
the same for TedigoUnaVaina in March 2026. Both now run on one shared FastAPI
service backed by MySQL.

My scope is the backend and the automation layer. The frontends are
template-based Next.js apps that consume the same API.

- **Founder & Sole Backend Developer @ MendozaByteSolution** (Independent Software Products) · 2025 – Present
  - [riptoforex.com](https://riptoforex.com) — Forex and crypto news
  - [tedigounavaina.info](https://tedigounavaina.info) — Spanish-language lifestyle content
  - One FastAPI backend, one MySQL database, two independent sites
- **Open-source contributor** — merged PR [#32346](https://github.com/mdn/translated-content/pull/32346) to Mozilla MDN Web Docs (Spanish localization, l10n-es)
- 📍 Newnan, GA — open to onsite or hybrid roles in the Atlanta area

**Open to:** Backend Engineer · Python Engineer · AI/LLM Integration Engineer

---

### What I've built

**The API** — 15 REST endpoints on FastAPI, serving both platforms from a
single `main.py`. MySQL underneath via SQLAlchemy 2.x, with raw SQL and PyMySQL
reserved for migrations and maintenance. The schema is four models
(`posts`, `categories`, `seo_meta`, `used_categories`) plus one many-to-many
association table — a normalized replacement for the WordPress content model.

**The automation layer** — 22,424 lines of Python across 111 files and 338
single-author commits. Roughly 1,300 of those lines are the API; the rest is
operational automation for publishing, SEO, and AI-assisted content workflows,
integrating Google Gemini, SerpAPI, Pexels, Telegram Bot API, X (Twitter) API,
Facebook Graph API, Google Search Console, Google Trends, DuckDuckGo, and
Cloudflare.

**Kenvi, the agent platform** — an eight-agent system built on the open-source
Agent-Zero framework. I designed the architecture, orchestration, and routing,
and wrote the custom skills and production integrations on top of upstream
components. Agent memory uses FAISS embeddings for semantic retrieval; the
runtime is containerized with Docker. It replaced an n8n workflow with a
12-step autonomous publishing pipeline. I fine-tuned a model on a custom
dataset of 3,130 domain-specific examples and route requests across Anthropic
Claude, OpenAI, Google Gemini, and local inference endpoints depending on the
workload.

**Deployment and operations** — getting an ASGI application to run through
Phusion Passenger on shared cPanel hosting, without rewriting the framework or
adding infrastructure. Migrating 803 media assets, repairing 329 broken links,
and re-linking 44 orphaned posts out of the old WordPress installs. Tracing an
indexing failure across DNS, Cloudflare, origin, and application layers down to
edge-level bot filtering, then writing verified-crawler rules that kept the
existing security controls intact.

**Security controls** — API key authentication, SlowAPI rate limiting, HTML
sanitization with Bleach, CORS, MIME and Pillow upload validation, and
edge-layer HSTS, CSP, and Permissions-Policy headers.

Both platforms are live, with 270 published articles across 8 categories.

---

### Tech Stack

#### Languages
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=for-the-badge&logo=gnu-bash&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

#### Backend & Data
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=for-the-badge&logo=sqlalchemy&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=for-the-badge&logo=pydantic&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)

REST API design · SQLAlchemy 2.x · raw SQL via `text()` · PyMySQL · schema design and migrations

#### AI / LLM
![Claude](https://img.shields.io/badge/Claude-D97757?style=for-the-badge&logo=anthropic&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini-8E75B2?style=for-the-badge&logo=google&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=for-the-badge&logo=ollama&logoColor=white)

**Multi-agent:** Agent-Zero · MCP (Model Context Protocol)
**Local inference:** ExLlamaV2 / TabbyAPI · Ollama · llama.cpp · LM Studio
**Retrieval:** FAISS
**Fine-tuning:** Unsloth · RunPod (A100)

#### Infrastructure
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)

cPanel · Phusion Passenger · a2wsgi · SlowAPI · Bleach · Pillow

#### Foundational
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)

**Languages:** Spanish (native) · English (professional working proficiency)

---

### Public Repositories

#### [CPU Simulator](https://github.com/kelvinmendoza59/cpu-simulator)
MIPS architecture simulator — registers, memory bus, cache, and instruction
pipeline, covered by unit tests.
**C · Python**

#### [TaskMaster Pro](https://github.com/kelvinmendoza59/TaskMaster-Pro)
Task manager built as the HarvardX CS50x final project. Session auth with
bcrypt and a REST API.
**Python · Flask · SQLAlchemy · SQLite** — [video demo](https://www.youtube.com/watch?v=stsZTSPVnDM)

#### [Movie Recommender](https://github.com/kelvinmendoza59/movie_recommender)
Recommendation system using a Trie for prefix-based genre search.
**Python**

#### [Millionaire Game](https://github.com/kelvinmendoza59/millionaire-game)
Object-oriented implementation of the quiz show as a CLI application.
**Python**

#### [Mozilla MDN Web Docs](https://github.com/mdn/translated-content/pull/32346)
PR #32346 — reviewed, approved, and merged into MDN's Spanish documentation.

The production backend for RiptoForex and TedigoUnaVaina is in a private
repository.

---

### Education & Credentials

**Máster de Desarrollo con Inteligencia Artificial** *(in progress — expected December 2026)*
Universidad Isabel I / BIG School, Spain
Título Propio, 6 ECTS. A Spanish professional university credential; not
equivalent to a U.S. graduate degree.

**Computer Science Professional Certification** — Codecademy, 2025
Seven proctored exams with live coding: programming fundamentals, data
structures, algorithms, trees and graphs, databases, computer architecture,
and mathematics for computer science.

**CS50x: Introduction to Computer Science** — HarvardX, 2025
Final project: [TaskMaster Pro](https://github.com/kelvinmendoza59/TaskMaster-Pro).

**Bash/Shell and Command Line** — MoureDev Pro, 2026

**Cybersecurity Fundamentals** — Codecademy, 2024

---

### Current Focus

- Extending automated test coverage across the platform API
- Deepening the agent memory and retrieval layer in Kenvi
- Fine-tuning workflows for domain-specific model performance
- Running two live platforms on infrastructure I maintain myself

---

### Contact

<p align="left">
  <a href="mailto:kelvinmendoza309@gmail.com">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
  <a href="https://www.linkedin.com/in/kelvinmendoza59" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="https://riptoforex.com" target="_blank">
    <img src="https://img.shields.io/badge/riptoforex.com-1e40af?style=for-the-badge&logoColor=white" alt="RiptoForex" />
  </a>
</p>

📍 Newnan, GA
