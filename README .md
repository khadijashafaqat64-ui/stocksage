# StockSage AI: Smart Kitchen Waste Reducer

A lazy kitchen manager for restaurants. Add ingredients (or paste a messy note) and StockSage flags what is expiring, suggests dishes, builds a supplier-wise shopping list, tracks waste cost, and writes a daily report.

Open-source AI at the core: a local open-weight model runs through [Ollama](https://ollama.com), so your stock and prices never leave your laptop.

## Features
- Expiring and expired ingredient alerts, with waste cost in Rs
- Dish suggestions (expiring items first), plus your own menu dishes
- Supplier-wise shopping list with cost estimates
- Daily inventory report (copy or print)
- Local AI: auto-fill stock from a note or shelf photo, and a morning brief with specials

## Run it
1. Download `stocksage.html` and open it in Chrome or Edge. No install or build step needed.
2. Click **Load sample data** to try it.

## Enable the local AI (optional)
```bash
ollama pull qwen2.5:3b
```
Windows PowerShell:
```powershell
$env:OLLAMA_ORIGINS="*"
ollama serve
```
Keep that window open, refresh the page, and set **Text model** to `qwen2.5:3b` (any Ollama chat model works). For shelf photos, also pull a vision model such as `llava`.

Without Ollama, everything except the AI card still works.

## Stack
Single HTML file, vanilla JavaScript, `localStorage`, Ollama for local inference. No backend.

## License
MIT
