## Jack H. Park

**Product Manager who builds the systems he specs.**

I work on the seam between product judgment and running software: turning the parts of PM work
that are actually procedural — sensing, framing, deciding, documenting — into systems with
explicit contracts, human approval gates, and telemetry, so the judgment part gets more room.

Most of what I build is an *operating layer*: the strategy, guardrails, and contracts live in
versioned documents; code is added only where it earns its place.

🌐 [jackhpark.com](https://www.jackhpark.com)

---

### What I'm building

**1. A PM intelligence system** — a multi-repo stack that runs a `SENSE → DECIDE → LEARN` loop.
Signals come in through an API, pass through a 7-stage analysis workflow with multi-agent persona
evaluation and human gates at each decision boundary, and land as durable decision artifacts.
Deliberately not an autopilot: every gate is a place a human says yes.

- an execution engine (stage state machine, gate transitions, artifact persistence)
- a reasoning-asset source (identity, product context, prompts, rubrics) kept separate from execution
- a knowledge base that records *how* decisions were actually made, not just what was decided
- an observatory dashboard — pipeline DAG, run drill-downs, freshness and integrity rules, LLM cost

**2. Agentic operations** — a versioned control plane for long-running agents: profiles, skills,
distribution policies, runbooks. Behavior lives in `SKILL.md` contracts rather than in code, which
makes agent changes reviewable as diffs. The same pattern drives an
[agentic brokerage trading layer](https://github.com/jack-h-park) built as a provider abstraction
with hard guardrails and human-in-the-loop execution — a small, bounded-risk domain is the honest
way to test whether an agent operating model actually holds up.

**3. Production RAG and LLM observability** —
[**jackhpark-studio**](https://github.com/jack-h-park/jackhpark-studio) is my portfolio platform and
my reference implementation: Next.js 15 + Notion CMS, a RAG chat assistant on Supabase/pgvector and
LangChain, configurable retrieval and guardrails, and full tracing through Langfuse and PostHog.
Built to be read as much as run.

---

### How I work

- **Contracts before code.** Layer boundaries, output shapes, and ownership get written down first.
- **Human gates on anything consequential.** Automation earns scope by being observable, not by being confident.
- **Documentation is architecture.** If the system map can't be read in one file, the system is wrong.
- **Don't promote a pattern until it repeats.** Write the playbook; add the abstraction only when a second consumer shows up.
- **Instrument from day one.** Cost, latency, drift, and freshness are product surfaces, not ops afterthoughts.

---

### Public repositories

| Repo | What it is |
|---|---|
| [**jackhpark-studio**](https://github.com/jack-h-park/jackhpark-studio) | Portfolio platform — Next.js 15, Notion CMS, production RAG chat, Langfuse + PostHog observability |
| [**ai-skills**](https://github.com/jack-h-park/ai-skills) | Reusable audit playbooks and routing contracts for AI-assisted engineering work |
| [**react-notion-x**](https://github.com/jack-h-park/react-notion-x) | Fork of the React renderer for Notion, used by the portfolio stack |

Much of the PM intelligence and agent-operations work lives in private repositories. Happy to walk
through the architecture, decision logs, or dashboards in a conversation.

---

### Stack

`TypeScript` · `Python` · `Next.js` · `React` · `Tailwind` · `Supabase / Postgres / pgvector` ·
`LangChain` · `Claude / OpenAI APIs` · `MCP` · `Langfuse` · `PostHog` · `Notion API` ·
`Cloudflare Workers & Pages` · `GitHub Actions`

---

📫 [jackhpark.com](https://www.jackhpark.com) · [LinkedIn](https://www.linkedin.com/in/jackhpark)
