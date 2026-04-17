# AI Engineering Gists

Snippets from building with LLMs: evaluations, agents, MCP servers, and the plumbing that makes model behavior measurable and debuggable.

---

## Evals & LLM Testing

| Gist | What it shows |
|------|---------------|
| [Multi-turn LLM attribution](https://gist.github.com/nehasriva/ccd0b4cdf6219c49de58cf853c629831) | Linear scan to find the earliest constraint violation in a failed conversation; position-weighted confidence; systemic failure detection |
| [Immutable conversation trace](https://gist.github.com/nehasriva/b19fb37ccf78a225ccd6b5c36bdca18e) | Frozen Pydantic models as a conversation value type; safe mutation via `slice / replace_turn / append_turn`; OpenAI/Langfuse format bridge |
| [Confidence calibration — isotonic regression](https://gist.github.com/nehasriva/513896b8760be078fcb841709346391a) | Map heuristic scores to true probabilities; serialisable `Calibrator` with `transform_result()` |
| [Prompt A/B testing — weighted scoring](https://gist.github.com/nehasriva/b725d6286b288f7ef3d23112e8373996) | Composite metric scoring so a single number doesn't pick the winner; surfaces per-metric deltas > 10% |
| [LLM eval notebook](https://gist.github.com/nehasriva/98013496cab5d264c0756b2a70a89718) | Parallel model runs with `ThreadPoolExecutor`; LLM-as-judge JSON rubric; regression detection by pivot |

---

## Agents & MCP

| Gist | What it shows |
|------|---------------|
| [Bootstrap a Vitest MCP server](https://gist.github.com/nehasriva/567d90a3d5d24346272ad76b96f4d13d) | JSON Schema tool catalogue; single dispatcher; consistent error envelopes; stdio transport |
| [MCP resources + prompt templates](https://gist.github.com/nehasriva/4be71679e8545bb69dfc37e4b70fad72) | The two MCP primitives most servers skip: URI-addressable resources (declared once, fetched on demand) and reusable prompt templates with typed arguments rendered server-side |

---

## By Language

| Language | Gists |
|----------|-------|
| **Python** | Multi-turn attribution · Immutable trace · Confidence calibration · Prompt A/B scoring |
| **TypeScript** | MCP server bootstrap · MCP resources + prompts |
| **Jupyter** | LLM eval notebook |

---

## Tags

`python` `typescript` `llm-evals` `multi-turn` `attribution` `pydantic`
`isotonic-regression` `mcp` `claude-api` `agents`
`promptfoo` `jupyter` `pandas` `openai` `langfuse` `tracing`
`structured-outputs` `llm-as-judge`
