<div align="center">

# Ciao, sono Achraf 👋

### AI Engineer · LLM & AI Agents

Costruisco sistemi basati su Large Language Model e agenti AI — dalla ricerca sul campo fino al deploy, passando per la parte che quasi nessuno mostra: farli funzionare in modo affidabile, testabile e sicuro.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/achraf-sobhi-37183434b/)

</div>

---

## Chi sono

Sono un AI Engineer junior/mid, in AIVolve, con base solida di sviluppo software full-stack. Il mio percorso è partito da autodidatta e in meno di due anni è diventato lavoro vero su problemi reali: sistemi multi-agente, pipeline di validazione, monitoraggio dei costi AI, interfacce conversazionali con streaming in tempo reale.

Non mi interessa mostrare demo che funzionano solo in teoria. Ogni progetto qui sotto ha un gate di qualità dietro: test automatici, dati puliti (mai credenziali o dati di clienti reali), documentazione pensata per essere letta da chi non ha il contesto che ho io.

## 🏆 The Silent Council — AMD Developer Hackathon ACT III

**[AIVolve-Team/the-silent-council](https://github.com/AIVolve-Team/the-silent-council)** · progetto di team AIVolve · 12–18 ottobre 2026

Un **consiglio di agenti AI che revisiona contratti commerciali**, in esecuzione su una GPU **AMD Instinct MI300X**. Tre esperti — legale, finanziario e rischio — leggono ciascuno la propria parte del contratto; un relatore, nel ruolo di avvocato del diavolo, scrive il verdetto: **firmare, negoziare o non firmare**, le clausole da segnalare con citazione esatta e i punti su cui gli esperti non sono d'accordo. L'ultima parola resta sempre a una persona, che decide su ogni dissenso dalla pagina del verdetto.

**L'idea centrale: gli agenti non si scrivono, si passano la memoria.** Invece di scambiarsi testo, ogni agente consegna al successivo un *messaggio latente* — la KV cache di ciò che ha letto e ragionato — firmato con **Ed25519** e verificato prima dell'uso. Lo stesso consiglio gira anche in modalità testo come baseline, e un'eval pre-registrata confronta le due modalità su benchmark pubblici di contratti (CUAD, ContractNLI, CLAUDETTE).

Intorno al motore:

- **Memoria istituzionale** — il playbook dell'azienda e i precedenti decisi dalle persone entrano in testa a ogni revisione: ogni scelta diventa un precedente per i contratti successivi.
- **Modalità visiva** — un ispettore PDF individua firme, timbri, sigle e scansioni; un esperto visivo (Gemma 4 31B) vede quelle pagine come immagini. Su domande non previste sulle pagine, la modalità "telepatica" ha risposto giusto 4 volte su 4, quella testuale 1 su 4.
- **ask_council** — il server tiene la memoria delle ultime revisioni in GPU (mai su disco) e risponde a nuove domande su un caso senza rileggere il contratto.
- **Integrazione reale** — i contratti arrivano via email tramite Evolus, il consiglio viene chiamato via **MCP** / HTTP e la persona riceve la notifica.
- **Routing per lunghezza** — Qwen3-14B per i contratti brevi, Gemma 4 31B per quelli lunghi.

`Python` · `PyTorch` · `Hugging Face Transformers` · `Qwen3` · `Gemma 4` · `AMD ROCm / MI300X` · `MCP` · `Ed25519` · `Vercel` · `GitHub Actions`

## 🚀 Progetti in evidenza

| Progetto | Cosa fa | Stack |
|---|---|---|
| **[The Silent Council](https://github.com/AIVolve-Team/the-silent-council)** — AMD Hackathon ACT III | Consiglio di agenti (legale, finanza, rischio + relatore) che revisiona contratti passandosi la memoria latente (KV cache firmata Ed25519) invece del testo; verdetto con clausole citate, dissensi e decisione finale umana | Python · PyTorch · Transformers · MCP · AMD ROCm |
| **[Sales Intelligence Agent](https://github.com/AshSobhiDev/sales-intelligence-agent)** — [demo live](https://sales-intelligence-agent-omega.vercel.app) | Scheduling copilot per PMI di servizi: propone orari, prepara la risposta, chiede sempre approvazione umana prima di inviare (prototipo, dati sintetici) | JavaScript (ES modules) |
| **[Venture Studio Pipeline](https://github.com/AshSobhiDev/venture-studio-pipeline)** | Orchestratore multi-agente che valida idee di business con gate di approvazione umana esplicito e test avversariali (prompt injection, input ambiguo) | Python · Hermes Agent |
| **[AI Usage Telemetry](https://github.com/AshSobhiDev/ai-usage-telemetry)** | Monitoraggio di consumo e costo di Claude Code / GitHub Copilot via OpenTelemetry, con dashboard Grafana/Loki/Prometheus | Python · Docker · Grafana |
| **[Intelligence Flux](https://github.com/AshSobhiDev/ai-chat-vue)** — [demo live](https://ai-chat-vue-six.vercel.app) | Chat AI con streaming token-per-token via Gemini API, riconoscimento vocale, animazioni reattive | Vue 3.5 · TypeScript · Pinia |
| **[TaskFlow Board](https://github.com/AshSobhiDev/kanban-vue)** — [demo live](https://kanban-vue-sandy.vercel.app) | Kanban board con drag & drop, dark/light mode, persistenza locale | Vue 3.5 · Pinia · Tailwind CSS |

## 🛠️ Stack

**Linguaggi & frontend**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Vue.js](https://img.shields.io/badge/Vue.js-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white)
![Angular](https://img.shields.io/badge/Angular-DD0031?style=flat-square&logo=angular&logoColor=white)

**AI & LLM**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging_Face_Transformers-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![MCP](https://img.shields.io/badge/MCP-000000?style=flat-square&logo=modelcontextprotocol&logoColor=white)
![Google Gemini](https://img.shields.io/badge/Gemini_API-8E75B2?style=flat-square&logo=googlegemini&logoColor=white)
![AMD ROCm](https://img.shields.io/badge/AMD_ROCm-ED1C24?style=flat-square&logo=amd&logoColor=white)

**Infra & DevOps**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![uv](https://img.shields.io/badge/uv-DE5FE9?style=flat-square&logo=uv&logoColor=white)

## 📊 Attività

<div align="center">

![GitHub stats](https://github-readme-stats.vercel.app/api?username=AshSobhiDev&show_icons=true&theme=default&hide_border=true&count_private=true)

</div>

---

<div align="center">

📩 Aperto a confronti, consigli e opportunità nell'AI engineering.

</div>
