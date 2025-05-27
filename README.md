# n8n-Codex Workflows

This repository contains the reference material, examples, and contract file used by **ChatGPT Codex** to generate **ready-to-import n8n JSON workflows**.

---

## 📁 Folder layout

```

.
├─ AGENTS.md                # Contract / system prompt for Codex
├─ docs/                    # Read-only knowledge base
│   ├─ n8n_cheat_sheet_guide.pdf
│   └─ n8n_tips_and_tricks.txt
│   └─ README.md           # Documentation for this folder (Codex must not write here)
├─ examples/                # Valid exported workflows (reference)
│   ├─ (various sample workflows: Gmail, Slack, agents, etc.)
└─ generated/               # ← Codex writes new workflows here

```

*Everything inside **docs/** and **examples/** is **read-only** for Codex;  
it must never edit these files.*

---

## 🚀 Quick start

1. **Clone** the repo and open it in your editor.  
2. Verify that each file in **examples/** imports into your local n8n instance (v 1.91.2).  
3. Commit any additional example workflows or docs you want Codex to reference.  
4. Push the repository to GitHub.

---

## 🛠️ Generating a workflow with ChatGPT Codex

1. In ChatGPT Codex, **select this repository** as the project.  
2. Codex automatically reads **AGENTS.md** as its system prompt.  
3. In the chat, write your user-level request, for example:

```

Create a workflow that watches Gmail, summarises each new email with GPT-4o,
stores the summary in Airtable, and posts a Slack notification.

```

4. Codex returns **raw JSON** (no Markdown fences).  
5. Save the JSON into **generated/**, e.g. `generated/gmail_to_airtable.json`
6. In n8n ➜ **Import** ➜ select the file ➜ test & run.

If the import fails, copy the n8n error and the faulty JSON back to Codex; it can usually fix the structure in a follow-up message.

---

## ✅ Requirements

| Tool | Version |
|------|---------|
| n8n  | **1.91.2** (May 2025) |
| OpenAI | **gpt-4o** (fallback **o1-mini**) |

---

## 🤝 Contributing

Feel free to open issues or pull requests if you have additional example workflows, updated cheat-sheets, or improvements to **AGENTS.md**.

---

## 📜 License

MIT
```
