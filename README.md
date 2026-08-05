### Hritik Datta

<p align="center">
  <b>Chief of Staff & GTM Lead @ <a href="https://pre6.ai">Pre6.ai</a></b> (Peak XV · General Catalyst)<br/>
  <sub>Bengaluru · I build LLM systems from first principles</sub>
</p>

<p align="center">
  AI companies split the work between people who sell the product and people who understand the machine.<br/>
  I never picked a side — and the public work below is the evidence for both claims.
</p>

---

### Why this profile exists

By day I run GTM at an enterprise AI company: pricing, positioning, pipeline, board reporting for Peak XV and General Catalyst. NRR 108% → 124%, win rates up ~40%, activation 26% → 41% — the kind of numbers a CEO wants in a board deck.

By night I ship the machinery underneath those products: a GPT in raw NumPy with every gradient derived by hand, an autograd engine, a tokenizer — each verified against ground truth and running live in the browser. If a CTO asks “do you actually understand the stack?”, the answer is a cloneable repo, not a slide.

**If you’re hiring for AI product leadership, GTM that can hold a technical thread, or someone who can evaluate LLM systems with receipts — let’s talk.**

---

### The LLM stack, from scratch

Three repos that build a language model's core machinery from first principles — pure Python/NumPy, no frameworks, every piece verified against ground truth, each with a **live in-browser demo**.

| | Project | What it builds | Proof |
|---|---|---|---|
| 1 | **[mosaic](https://github.com/Hritikd/mosaic)** | The **tokenizer** — train a real byte-pair-encoding tokenizer on your own text and watch strings break into token tiles. | lossless `decode(encode(x)) == x` invariant · **[live studio](https://hritikd.github.io/mosaic/)** |
| 2 | **[nabla](https://github.com/Hritikd/nabla)** | The **autograd engine** — reverse-mode automatic differentiation, with a visualizer that animates gradients flowing backward through the graph. | gradient-checked to ~1e-10 · **[live demo](https://hritikd.github.io/nabla/)** |
| 3 | **[loom](https://github.com/Hritikd/loom)** | The **GPT itself** — a transformer in pure NumPy, every gradient derived *by hand*, trained on Shakespeare. Generate text and inspect what each attention head looked at. | hand-derived gradients checked to ~1e-8 · KV-cache decode proven identical to full forward · **[live demo](https://hritikd.github.io/loom/)** |

### LLM engineering, the unglamorous parts

The half of AI products that decides whether they survive real users. Zero-dependency, deterministic, tested — clone and run in minutes, no API keys.

| Project | What it does |
|---|---|
| **[tinycoder](https://github.com/Hritikd/tinycoder)** | A real coding agent in ~570 lines — the agentic loop behind Cursor/Claude Code, from scratch: tool use, sandboxed workspace, confirmation gates. Fully unit-tested via an injected fake model client. |
| **[stencil](https://github.com/Hritikd/stencil)** | Constrained decoding — compiles a JSON Schema to a DFA and masks tokens so invalid LLM output is *impossible* (100% valid by construction vs ~0% unconstrained). **[Live demo](https://hritikd.github.io/stencil/)** |
| **[winnow](https://github.com/Hritikd/winnow)** | Budget-aware context compression for RAG/agents — BM25 relevance + MMR diversity packs the highest-signal chunks into a token budget (0.75 vs 0.19 gold recall against truncation). **[Live demo](https://hritikd.github.io/winnow/)** |
| **[introspect-mcp](https://github.com/Hritikd/introspect-mcp)** | MCP server that stops coding agents hallucinating APIs — introspects the *exact* package versions installed in your project and serves real signatures and source over MCP. |

<details>
<summary><b>More</b> — retrieval, safety, evals, and systems work</summary>

- **[warren](https://github.com/Hritikd/warren)** — from-scratch HNSW vector index (the algorithm behind FAISS/Qdrant): recall@10 ≥ 0.99 scanning ~5% of the database · [live demo](https://hritikd.github.io/warren/)
- **[mend](https://github.com/Hritikd/mend)** — repairs malformed LLM JSON (fences, trailing commas, truncation): 16/16 real-world defects recovered vs stdlib's 0 · [live playground](https://hritikd.github.io/mend/)
- **[semcache](https://github.com/Hritikd/semcache)** — semantic cache for LLM calls: similar prompt in, cached response out; pluggable embedders/stores, TTL, LRU
- **[verdict](https://github.com/Hritikd/verdict)** — adversarial LLM red-teaming: PAIR, Crescendo, and injection attacks with attack-success-rate reports
- **[hermes](https://github.com/Hritikd/hermes)** — test-time compute scaling: o1-style reasoning search via process reward models, MCTS, beam search
- **[agent-evals-lab](https://github.com/Hritikd/agent-evals-lab)** — evaluation workbench for agent reliability with a trace-inspection dashboard · [live demo](https://hritikd.github.io/agent-evals-lab/)
- **[rag-safety-gateway](https://github.com/Hritikd/rag-safety-gateway)** — scans RAG context for prompt injection, secrets, and PII before it reaches a model · [live demo](https://hritikd.github.io/rag-safety-gateway/)
- **[continuum](https://github.com/Hritikd/continuum)** — self-improving ML pipeline: production signals → active-learning curation → incremental LoRA with EWC regression guards
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

### What I want to talk about

- Pricing, packaging, and positioning for AI products that actually retain
- Eval bars that gate releases — quality as a release criterion, not a hope
- LLM internals, agent reliability, and the boring infrastructure that keeps demos from dying in production
- Roles where GTM/product leadership and technical depth are the same job

Write me. I read everything.

<p align="center">
  <a href="https://hritikd.github.io"><img src="https://img.shields.io/badge/Website-hritikd.github.io-B4540A?style=flat-square&logo=googlechrome&logoColor=white" /></a>
  <a href="https://www.linkedin.com/in/hritikdatta/"><img src="https://img.shields.io/badge/LinkedIn-hritikdatta-0A66C2?style=flat-square&logo=linkedin&logoColor=white" /></a>
  <a href="https://x.com/hritikd05"><img src="https://img.shields.io/badge/X-@hritikd05-111?style=flat-square&logo=x&logoColor=white" /></a>
  <a href="mailto:hritikdatta2403@gmail.com"><img src="https://img.shields.io/badge/Email-hritikdatta2403%40gmail.com-111?style=flat-square&logo=gmail&logoColor=white" /></a>
</p>

<p align="center"><sub>Open to conversations with founders, CTOs, and operators building serious AI products.</sub></p>
