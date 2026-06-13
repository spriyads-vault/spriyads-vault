# Sathishka Priyad

AI Product, built on a decade of shipping the engineering underneath it.
I decide what an AI system has to prove before it ships, then build the
eval and retrieval infrastructure that proves it.

Currently product lead on Crado, a compliance intelligence platform for
deep-tech hardware. Live at app.crado.io.

Production track record: 2M-user REST APIs (Wiley) · 3,500 RPS on AWS EKS
(B&S Group) · 60% latency reduction via LangSmith profiling · 85% error
reduction via Pydantic schema guardrails.

London, UK work authorisation · sash.priyad@gmail.com

---

## The product call I'm proudest of

Crado verifies regulatory standards across markets. The obvious design used
an LLM as the judge on every clause. I cut it.

A deterministic critic stage now matches the LLM judge at F1 = 1.000 across
468 executions, by construction, with zero model calls in the verification
path. That decision removed per-query cost and latency from the most
frequent operation in the product, and made the output auditable, which a
compliance buyer requires and an LLM judge cannot give.

Supersession detection runs at 0.88 against baselines of 0.42 to 0.61.
Methodology and benchmark detail: [link → benchmark write-up]

---

## How I think about AI products

**Decide what earns its cost.** Most LLM features don't survive a real
eval-versus-cost comparison. My job is to run that comparison before the
build, not after the invoice.

**Make the eval the spec.** I define what the system must prove, then the
harness is the contract. Online evals, latency and cost profiling,
deterministic test sets.

**Cut more than I add.** The deterministic-critic decision above is the
pattern: the strongest product move is usually the thing you remove.

---

## The engineering I built to back the judgement

**Agentic systems that self-correct.** Stateful LangGraph pipelines with
critic loops, schema-validated tool calls, observability from the first
commit.

**Retrieval that routes instead of brute-forcing.** Reciprocal Rank Fusion
over dense and sparse, semantic routing per query class, hallucination
attribution scoring.

### Selected work
- **Crado** — multi-market hardware compliance intelligence. LangGraph, Next.js, Supabase.
- **Customer Support Agent** — four-stage pipeline with full LangSmith observability and async online evals.
- **Adaptive RAG Engine** — semantic router dispatching to FAISS, BM25, or knowledge-graph retrieval per query class.
- **InferBench** — local SLM benchmarking: TTFT, TPS, VRAM delta, quality recall across 15 deterministic prompts.

---

London, UK · sash.priyad@gmail.com · github.com/spriyads-vault
