<h1 align="center">Hritik Datta</h1>

<p align="center">
  <b>Product @ <a href="https://github.com/pre6ai">Pre6 AI</a></b> &nbsp;·&nbsp; I build the machinery behind AI products.
</p>

<p align="center">
  <i>Product by title, builder by craft — I design AI products and ship the engineering behind them:
  from-scratch LLM internals, agent systems, and the infrastructure that makes them reliable.</i>
</p>

---

### The LLM stack, from scratch

Three repos that build a language model's core machinery from first principles — pure Python/NumPy,
no frameworks, every piece verified against ground truth, each with a **live in-browser demo**.

| | Project | What it builds | Proof |
|---|---|---|---|
| 1 | **[mosaic](https://github.com/Hritikd/mosaic)** | The **tokenizer** — train a real byte-pair-encoding tokenizer on your own text and watch strings break into token tiles. | lossless `decode(encode(x)) == x` invariant · **[live studio](https://hritikd.github.io/mosaic/)** |
| 2 | **[nabla](https://github.com/Hritikd/nabla)** | The **autograd engine** — reverse-mode automatic differentiation, with a visualizer that animates gradients flowing backward through the graph. | gradient-checked to ~1e-10 · **[live demo](https://hritikd.github.io/nabla/)** |
| 3 | **[loom](https://github.com/Hritikd/loom)** | The **GPT itself** — a transformer in pure NumPy, every gradient derived *by hand*, trained on Shakespeare. Generate text and inspect what each attention head looked at. | hand-derived gradients checked to ~1e-8 · KV-cache decode proven identical to full forward · **[live demo](https://hritikd.github.io/loom/)** |

### LLM engineering, the unglamorous parts

The half of AI products that decides whether they survive real users. Zero-dependency, deterministic,
tested — clone and run in minutes, no API keys.

| Project | What it does |
|---|---|
| **[tinycoder](https://github.com/Hritikd/tinycoder)** | A real coding agent in ~570 lines — the agentic loop behind Cursor/Claude Code, from scratch: tool use, sandboxed workspace, confirmation gates. Fully unit-tested via an injected fake model client. |
| **[stencil](https://github.com/Hritikd/stencil)** | Constrained decoding — compiles a JSON Schema to a DFA and masks tokens so invalid LLM output is *impossible* (100% valid by construction vs ~0% unconstrained). **[Live demo](https://hritikd.github.io/stencil/)** |
| **[winnow](https://github.com/Hritikd/winnow)** | Budget-aware context compression for RAG/agents — BM25 relevance + MMR diversity packs the highest-signal chunks into a token budget (0.75 vs 0.19 gold recall against truncation). **[Live demo](https://hritikd.github.io/winnow/)** |
| **[introspect-mcp](https://github.com/Hritikd/introspect-mcp)** | MCP server that stops coding agents hallucinating APIs — introspects the *exact* package versions installed in your project and serves real signatures and source over MCP. |

<details>
<summary><b>More</b> — retrieval, safety, evals, and systems work</summary>
<br/>

- **[warren](https://github.com/Hritikd/warren)** — from-scratch HNSW vector index (the algorithm behind FAISS/Qdrant): recall@10 ≥ 0.99 scanning ~5% of the database · [live demo](https://hritikd.github.io/warren/)
- **[mend](https://github.com/Hritikd/mend)** — repairs malformed LLM JSON (fences, trailing commas, truncation): 16/16 real-world defects recovered vs stdlib's 0 · [live playground](https://hritikd.github.io/mend/)
- **[semcache](https://github.com/Hritikd/semcache)** — semantic cache for LLM calls: similar prompt in, cached response out; pluggable embedders/stores, TTL, LRU
- **[verdict](https://github.com/Hritikd/verdict)** — adversarial LLM red-teaming: PAIR, Crescendo, and injection attacks with attack-success-rate reports
- **[hermes](https://github.com/Hritikd/hermes)** — test-time compute scaling: o1-style reasoning search via process reward models, MCTS, beam search
- **[agent-evals-lab](https://github.com/Hritikd/agent-evals-lab)** — evaluation workbench for agent reliability with a trace-inspection dashboard · [live demo](https://hritikd.github.io/agent-evals-lab/)
- **[rag-safety-gateway](https://github.com/Hritikd/rag-safety-gateway)** — scans RAG context for prompt injection, secrets, and PII before it reaches a model · [live demo](https://hritikd.github.io/rag-safety-gateway/)
- **[gemma4-multi-agent](https://github.com/Hritikd/gemma4-multi-agent)** — supervisor + 4 specialist agents with live reasoning traces (LangGraph + Gemini)
- **[tally](https://github.com/Hritikd/tally)** — streaming statistics in bounded memory: Welford, reservoir sampling, Count-Min sketch, Misra-Gries

</details>

---

### How I build

```text
Derived, not imported     →  if I claim to understand it, I can build it from scratch
Verified, not vibes       →  gradients checked numerically, benchmarks reproducible, invariants unit-tested
Honest READMEs            →  every project states its limitations before you find them
Reviewable in 60 seconds  →  clone, run, understand — zero API keys to start
```

### Stack

`Python` · `NumPy` · `TypeScript` · `LangGraph` · `React` · `Streamlit` · `MCP` · `pytest` · `GitHub Actions` · `uv`

---

<p align="center">
  <a href="https://www.linkedin.com/in/hritikdatta/"><img src="https://img.shields.io/badge/LinkedIn-hritikdatta-0A66C2?style=flat-square&logo=linkedin&logoColor=white" /></a>
  <a href="https://x.com/hritikd05"><img src="https://img.shields.io/badge/X-@hritikd05-111?style=flat-square&logo=x&logoColor=white" /></a>
  <a href="mailto:hritikdatta2403@gmail.com"><img src="https://img.shields.io/badge/Email-hritikdatta2403%40gmail.com-111?style=flat-square&logo=gmail&logoColor=white" /></a>
</p>

<p align="center"><sub>Open to conversations on AI agent engineering, LLM internals, and evals.</sub></p>
