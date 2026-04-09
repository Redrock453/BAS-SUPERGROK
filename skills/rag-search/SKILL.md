---
name: rag-search
description: Search the local Qdrant knowledge base. Use when user asks questions about projects, configs, or past work.
---

# RAG Search Skill

## When to use
- Вопросы о проектах (grim-fpv-ai, Vika_Ok, TacticalMesh)
- Поиск конфигураций и настроек
- История решений и команд

## Usage
```bash
# Поиск по базе знаний
python3 ~/ingest.py --search "твой вопрос" --top 5

# Если Qdrant не запущен
cd ~/bin && ./qdrant &
```

## Qdrant info
- URL: http://localhost:6333
- Collection: brain
- Dashboard: http://localhost:6333/dashboard
