# AGENTS.md — BAS-SUPERGROK

## Команды
- Поиск по базе знаний: `python3 ~/ingest.py --search "запрос" --top 5`
- Логи bash: `~/BAS-SUPERGROK/.logs/bash.log`
- Запустить агента: `python3 ~/run_agent.py [liliya|sofia|angelochek|victoria] "задача"`

## Инфраструктура
| Сервис | Адрес |
|--------|-------|
| LiteLLM | 100.68.33.14:4000 |
| Qdrant | 100.68.33.14:6333 |
| Ollama | localhost:11434 (gemma2:2b) |
| VPS | ssh claude@100.68.33.14 (без ключа, Tailscale) |

## Агенты
- **liliya** — оркестратор, планирование
- **sofia** — исполнитель bash/python
- **angelochek** — RAG поиск по Qdrant (коллекция: brain)
- **victoria** — DevOps, SSH

## Правила
- Язык: русский, технический
- Деструктивные операции — одно подтверждение
- SSH внутри сети — без ключей, только через Tailscale IP