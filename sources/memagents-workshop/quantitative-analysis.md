# MemAgents Workshop (ICLR 2026) — Quantitative Analysis of 70 Papers

## 1. Paper Types (N=70)

| Type | Count | % |
|------|-------|---|
| Architecture/System | 46 | 65.7% |
| Evaluation/Analysis | 8 | 11.4% |
| Benchmark | 8 | 11.4% |
| Theoretical/Framework | 7 | 10.0% |
| Survey | 1 | 1.4% |

**Key finding:** Two-thirds of the workshop focuses on building new systems; benchmarks and evaluations together account for only 23%.

## 2. Memory Types (CoALA taxonomy, papers may address multiple)

| Memory Type | Papers | % of 70 |
|-------------|--------|---------|
| Episodic | 41 | 58.6% |
| Semantic | 39 | 55.7% |
| Working | 20 | 28.6% |
| Procedural | 17 | 24.3% |

**Key finding:** Episodic and semantic memory dominate (>55% each), while procedural memory — how to perform tasks — is addressed by only 24% of papers. Working memory (context window management) appears in 29%.

## 3. Primary Problems Addressed

| Problem Category | Papers | % | Example papers |
|-----------------|--------|---|----------------|
| Context/working memory management | 15 | 21.4% | 9,11,17,21,24,32,40,47,53,55,58,69 |
| Retrieval quality/failure | 12 | 17.1% | 6,7,10,13,15,26,35,46,54,56,64 |
| Cross-session learning/transfer | 12 | 17.1% | 1,4,14,16,23,28,37,44,65,66,67,70 |
| Memory consolidation/organization | 10 | 14.3% | 2,5,27,33,34,38,41,42,48,62 |
| Forgetting/staleness | 5 | 7.1% | 20,29,45,51,52 |
| Memory scalability | 4 | 5.7% | 22,25,49,50 |
| Benchmark design | 4 | 5.7% | 57,59,63,68 |
| Memory security/safety | 3 | 4.3% | 18,43,60 |
| Other | 5 | 7.1% | 8,12,30,36,39 |

**Key finding:** Context management (21%) and retrieval (17%) together account for 38% — the field is still solving *where* and *how* to store and find memories. Cross-session learning (17%) is the third-largest category but temporal aspects within it are rare.

## 4. Method Categories

| Method | Papers | % |
|--------|--------|---|
| Retrieval-augmented (focus on retrieval pipeline) | 14 | 20.0% |
| Graph-based memory (KG, event graphs) | 8 | 11.4% |
| Hierarchical consolidation | 7 | 10.0% |
| Experience replay / experiential learning | 6 | 8.6% |
| Extraction-based (fact/memory extraction) | 6 | 8.6% |
| KV-cache compression | 5 | 7.1% |
| Embedding-based | 4 | 5.7% |
| RL-based memory management | 4 | 5.7% |
| Attention-based | 3 | 4.3% |
| Other (Bayesian, thermodynamic, action compression, etc.) | 13 | 18.6% |

**Key finding:** Retrieval-augmented approaches dominate (20%), followed by graph-based memory (11%) and hierarchical consolidation (10%). RL-based memory management is emerging (6%) but still early.

## 5. Temporal Mechanisms

| Temporal Level | Papers | % |
|----------------|--------|---|
| No temporal mechanism | 38 | 54.3% |
| Shallow (timestamps, basic ordering, recency) | 24 | 34.3% |
| Moderate (decay curves, temporal re-ranking) | 5 | 7.1% |
| Deep (validity intervals, versioning, temporal ontology) | 3 | 4.3% |

**Detailed breakdown of the 32 papers with any temporal mechanism:**
- Timestamps only: 10, 36, 44, 61, 69 (5 papers)
- Temporal ordering: 4, 20, 26, 35, 46, 59, 62, 63 (8 papers)
- Recency buffer/weighting: 6, 9, 11, 38, 48, 52 (6 papers)
- Sliding window: 2, 5 (2 papers)
- Temporal anchors/categories: 12, 47 (2 papers)
- Temporal decay: 34, 42, 43, 49 (4 papers)
- Temporal re-ranking: 51 (1 paper)
- Life arcs/time windows: 57 (1 paper)
- Validity intervals: 21 (1 paper)
- Decay + versioning: 27 (1 paper — theoretical)
- Temporal KG: 68 (1 paper)

**Key finding:** 54% of papers have no temporal mechanism at all. Of the 46% with some temporal aspect, the vast majority (34%) use only basic timestamps or ordering. Only 4% (3 papers) implement deep temporal reasoning with validity intervals or versioning — and one of those is theoretical. **Zero papers implement bi-temporal tracking or temporal consistency checking.**

## 6. Benchmarks Used (most popular)

| Benchmark | Papers using it | % |
|-----------|----------------|---|
| LoCoMo | 13 | 18.6% |
| LongMemEval | 7 | 10.0% |
| SWE-Bench variants | 5 | 7.1% |
| HotpotQA | 4 | 5.7% |
| ALFWorld | 3 | 4.3% |
| GSM8K | 3 | 4.3% |
| MATH/MATH-500 | 3 | 4.3% |
| MuSiQue | 3 | 4.3% |
| 2WikiMultiHopQA | 3 | 4.3% |
| LongBench | 3 | 4.3% |
| WebArena | 2 | 2.9% |
| AppWorld | 2 | 2.9% |

30+ papers (43%) introduce their own novel/custom benchmarks.

**Key finding:** LoCoMo is the de facto standard (19%), but the benchmark landscape is highly fragmented — 43% of papers use custom benchmarks, making cross-paper comparison difficult.

## 7. Application Domains

| Domain | Papers | % |
|--------|--------|---|
| General-purpose | 25 | 35.7% |
| Conversational | 18 | 25.7% |
| QA / Information retrieval | 9 | 12.9% |
| Software Engineering | 4 | 5.7% |
| Web agents | 4 | 5.7% |
| Robotics | 2 | 2.9% |
| Multi-agent | 2 | 2.9% |
| Other (finance, IT ops, narrative) | 6 | 8.6% |

**Key finding:** SE-specific papers represent only 6% of the workshop (papers 4, 23, 40, 55). The field is heavily skewed toward conversational (26%) and general-purpose (36%) settings.

## 8. Memory Operations

| Operation | Papers | % |
|-----------|--------|---|
| Retrieve | 59 | 84.3% |
| Write | 55 | 78.6% |
| Read | 52 | 74.3% |
| Consolidate | 22 | 31.4% |
| Update | 16 | 22.9% |
| Forget | 13 | 18.6% |

**Key finding:** While 85% address retrieval and 79% address writing, only 31% tackle consolidation, 23% handle updates, and just 19% implement explicit forgetting. The write-retrieve cycle dominates; higher-order operations are under-explored.

## 9. Cross-cutting Insights

### The Episodic-Temporal Paradox
59% of papers address episodic memory, yet only 11% implement temporal mechanisms beyond basic timestamps. The community recognizes episodic memory's importance but overwhelmingly treats episodes as unordered collections rather than temporally situated experiences.

### The Consolidation Gap
Only 31% of papers address memory consolidation — yet consolidation is precisely where temporal reasoning matters most. Without consolidation, memories accumulate without integration, leading to the retrieval failures that 17% of papers try to solve downstream.

### The Forgetting Deficit
Only 19% implement explicit forgetting. Combined with the 7% addressing staleness, this means >73% of memory systems are accumulate-only, with no mechanism to handle outdated information.

### The Benchmark Fragmentation Problem
43% of papers use custom benchmarks, making systematic comparison impossible. LoCoMo (19%) is the closest to a standard, but it evaluates conversational memory only. No benchmark evaluates cross-session learning, temporal consistency, or memory governance.

### Security as Afterthought
Only 3 papers (4%) address memory security — yet MINJA (#60) demonstrates 98% injection success rate on shared memory agents. Memory poisoning is a critical gap.

## 10. What's Absent: Under-Explored Aspects

| Aspect | Papers | % of 70 | Key papers |
|--------|--------|---------|------------|
| Deep temporal (validity intervals, versioning) | 3 | 4.3% | #21, #27, #57 |
| Collaborative/shared memory | 5 | 7.1% | #03, #12, #21, #44, #60 |
| Memory provenance/explainability | 4 | 5.7% | #24, #38, #54, #61 |
| User control over memory | 3 | 4.3% | #37, #51, #61 |
| Memory security/safety | 3 | 4.3% | #18, #43, #60 |
| Multi-modal memory | 2 | 2.9% | #12, #46 |
| Causal/counterfactual memory | 2 | 2.9% | #51, #59 |
| Memory interoperability/standards | 1 | 1.4% | #04 (transplant protocol only) |
| Privacy/GDPR/right-to-delete | 0 | 0% | — |

**Key finding:** The dominant research focus is single-agent, text-only, write-retrieve memory for individual sessions. Collaborative memory (7%), provenance (6%), user agency (4%), multimodal (3%), causal (3%), and interoperability (1%) are dramatically under-represented. **Zero papers address privacy/GDPR-compliant deletion as a primary contribution.** The framing is overwhelmingly agent-autonomous — the agent decides what to remember. User control is an afterthought.

## 11. SE-Specific Papers (4/70 = 5.7%)

| # | Title | Focus |
|---|-------|-------|
| 4 | Memory Transplants | Cross-domain transfer (code→math) |
| 23 | MemGrad | Multi-agent SE with dual memory |
| 40 | CoMem | Context compression for SWE-Bench |
| 55 | Evaluating AGENTS.md | Repository context files (negative result) |

None of the 4 SE papers addresses temporal versioning, API staleness, or decision provenance.
