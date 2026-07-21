# Speaker Script: Graph-Structured Memory for Cognitive Agents
*From Knowledge Graphs to Non-Euclidean Geometry*

**Target duration:** 10 minutes + 5 minutes discussion
**Venue:** FGWM Workshop @ KI 2026, Bremen

---

## [Title Slide]
*~15 seconds*

Good morning everyone. My name is Michael Banf from Perelyn in Munich. Today I will be presenting our survey on graph-structured memory for cognitive agents, and how non-Euclidean geometry could address some of the fundamental limitations we are seeing in current systems.

---

## [Overview]
*~15 seconds*

We will start with why graph memory matters, then look at the taxonomy of architectural patterns we identified, followed by the retrieval landscape. Then we will explore what we call the geometric frontier, and close with the key takeaway.

---

## --- Section: Why Graph Memory? ---
*~5 seconds*

Let us start with the motivation.

---

## Slide 1: The Limits of Flat Memory
*~60 seconds*

Large language model agents need memory that spans sessions, tracks how knowledge changes over time, and supports multi-hop reasoning. The dominant approaches today are vector stores, key-value extraction, or simply compressing everything into an ever-growing context window. These work reasonably well for factual recall, but they fail systematically on three critical capabilities.

First, temporal reasoning. When did something change? Is this information still valid? Second, multi-hop inference. Connecting facts across multiple reasoning steps. And third, knowledge evolution. Updating beliefs when the world changes.

The benchmarks quantify this deficit clearly. LoCoMo-Plus reports cognitive accuracy below twenty-five percent across Mem0, Letta, and Zep. MemoryAgentBench finds all methods below seven percent on multi-hop conflict resolution. These are not minor gaps. They represent fundamental limitations of flat memory representations.

---

## Slide 2: Graph Memory: A Different Strategy
*~50 seconds*

Graph-structured memory offers a fundamentally different approach. Instead of compressing everything into the context window, you store knowledge in a graph and retrieve selectively.

Entities and relations become first-class objects. Temporal intervals live directly on edges. And retrieval becomes a graph topology problem rather than a similarity search problem.

The results are compelling. Multi-strategy graph systems achieve over ninety-one percent retrieval accuracy, compared to forty-nine percent for extraction-based systems on the LongMemEval benchmark.

On the right you can see the structural progression from flat memory to knowledge graphs to hierarchical graphs and ultimately to geometric representations, which is where we argue the field needs to go.

---

## --- Section: Graph Memory Taxonomy ---
*~5 seconds*

So what does the landscape of graph-based memory systems actually look like?

---

## Slide 3: Six Architectural Patterns
*~70 seconds*

We surveyed over thirty systems published between 2023 and 2026 and identified six architectural patterns.

The first four are established. Entity-relation knowledge graphs are the most common, representing memory as typed subject-relation-object triples. Systems like GraphRAG and AriGraph fall into this category. Hierarchical event graphs add episodic and semantic layers with cross-layer edges. Systems like GAM and MemFly implement this. Bipartite and associative graphs take a lighter approach, linking chunks and queries directly. And multi-graph composites like MAGMA maintain several orthogonal views simultaneously.

Two emerging patterns push beyond pairwise relations. Hypergraph memory systems use hyperedges for n-ary facts and multi-step reasoning chains. And procedural strategy graphs encode agent trajectories directly, where interestingly a trained four-billion parameter model with graph memory outperforms a baseline eight-billion parameter model.

One key finding: entity-relation knowledge graphs account for sixty percent of all surveyed systems. Non-knowledge-graph structures remain surprisingly rare.

---

## Slide 4: The Temporal Grounding Deficit
*~50 seconds*

Despite temporal reasoning being the central promise of graph-based memory, fifty-seven percent of surveyed systems implement no temporal mechanism at all. Only twenty percent go beyond simple timestamps.

The most complete solution is Graphiti from Zep, which uses a bi-temporal model distinguishing event time from ingestion time, with validity intervals on every edge. Other approaches include RecallM with temporal windows and MemoTime with time tree structures.

But critical capabilities remain missing. No system tracks when abstracted semantic knowledge becomes outdated. Continuous-time evolution is largely unexplored. And principled temporal fusion, meaning combining temporal information with entity and relation representations in a mathematically sound way, is an open problem. This is where geometric techniques become relevant, as we will see shortly.

---

## --- Section: Retrieval Spectrum ---
*~5 seconds*

Let us look at how retrieval works across these systems.

---

## Slide 5: From Graph Algorithms to Learned Retrieval
*~70 seconds*

Memory retrieval over graphs spans a wide spectrum. The dominant approaches are training-free. Personalized PageRank, Leiden community detection, exponential recency decay. These run in ten to one hundred fifty milliseconds, work on any graph, and are what every deployed system uses.

Production systems go further by combining multiple pathways. Hindsight, for example, runs semantic search, keyword matching, graph traversal, and temporal filtering simultaneously, fusing the results via a cross-encoder. This achieves over ninety-one percent accuracy on the LongMemEval benchmark.

Reinforcement learning based approaches learn to optimize edge weights or memory operations, showing promising results. But graph neural network message passing, which you might expect to dominate, appears in only a handful of systems. The reasons include cold start problems, lack of retrieval labels, and the fact that graphs evolve faster than models can be retrained.

One striking finding across the literature, though we should note these comparisons are across independently reported benchmarks: graph-structured memory disproportionately benefits smaller models. GAM achieves plus thirty-nine percent F1 improvement at seven billion parameters, but only plus seven percent at GPT-4o scale. Graph structure appears to substitute for model scale.

---

## --- Section: The Geometric Frontier ---
*~5 seconds*

Now let us get to the part that we think opens up particularly interesting research directions.

---

## Slide 6: Why Geometry Matters
*~60 seconds*

All graph-based memory systems we surveyed embed their graphs in flat Euclidean space. But here is the problem: memory graphs are inherently hierarchical and tree-like. Euclidean volume grows polynomially, but tree branching grows exponentially. As the memory graph grows, Euclidean spaces cannot separate what the graph distinguishes. Representations collapse into a low-dimensional subspace. This is what we call semantic collapse.

The intuition behind the geometric solution is actually quite simple. Hyperbolic space has exponential volume growth, which naturally matches the exponential branching of hierarchical structures. Abstract topics embed near the center, specific episodic facts near the boundary, and the hierarchy is preserved by the geometry itself.

Curvature diagnostics provide another tool. They can flag edges where retrieval is likely to degrade, acting as a bottleneck detector, without any training at all.

And recent evidence makes this even more compelling: researchers have shown that large language model token embeddings already exhibit substantial negative Ricci curvature, suggesting that the models' internal representations are naturally hyperbolic. So matching the memory embedding space to the model's intrinsic geometry is a well-motivated direction.

---

## Slide 7: Three Geometric Techniques
*~60 seconds*

Let me highlight three concrete techniques.

First, discrete Ricci curvature. This is a per-edge diagnostic that tells you where information gets squeezed through bottleneck edges during multi-hop retrieval, a phenomenon called over-squashing. It is training-free, runs in linear time in the number of edges, and can be applied to any existing graph-memory system as a diagnostic layer.

Second, hyperbolic embeddings. These are a drop-in replacement for Euclidean entity representations. Systems like HyperbolicRAG and HypRAG have already demonstrated gains on hierarchy-aware retrieval tasks. The key advantage is that hierarchical separation is maintained as the graph grows, avoiding the semantic collapse problem.

Third, Lie group manifolds for temporal knowledge fusion. The challenge with temporal knowledge graphs is that entities, relations, and timestamps live in fundamentally different mathematical spaces, making direct fusion difficult. Lie groups, specifically their tangent space called the Lie algebra, provide a principled way to project these heterogeneous factors into a common vector space where standard neural network layers can process them.

Additionally, for memory graphs that have mixed topology, some parts tree-like, others more clique-like, mixed-curvature product spaces can assign different geometries to different regions.

---

## Slide 8: Concrete Example: Enhancing Graphiti/Zep
*~50 seconds*

To make this tangible, consider how Graphiti from Zep, the strongest bi-temporal system in our survey, could be geometrically enhanced.

Step one: compute Forman-Ricci curvature over its knowledge graph. This flags negatively curved bridge edges where multi-hop retrieval is likely to degrade. It provides an automatic diagnostic for the cognitive accuracy ceiling, and it requires no training whatsoever.

Step two: replace its Euclidean entity embeddings with Poincare ball embeddings. Now abstract concepts like project goals embed near the origin, while specific facts like meeting notes from June third sit near the boundary. Hierarchical separation is preserved as the graph grows.

Step three: fuse its temporal validity intervals with entity and relation embeddings via rotation matrices. This enables the system to answer not just what was stored, but when, and how beliefs evolved over time, without dedicated temporal query logic.

The important point is that none of these modifications require retraining the underlying large language model. They operate entirely on the memory layer itself.

---

## --- Section: Takeaway ---
*~5 seconds*

Let me close with the key takeaway.

---

## Slide 9: Key Takeaway
*~50 seconds*

Our central argument is that the structural limitations we see in graph-based agent memory, the cognitive accuracy ceilings, semantic collapse as memory grows, and the temporal reasoning deficits, are not just algorithmic shortcomings. They are consequences of a geometric mismatch between the inherently non-flat topology of memory graphs and the flat Euclidean spaces in which they are currently embedded.

Graph memory works. Multi-strategy retrieval reaches top benchmark scores, and graph structure disproportionately benefits smaller models. The temporal grounding deficit, with fifty-seven percent of systems having no temporal mechanism, is the most urgent gap. And geometric techniques from adjacent fields, knowledge graph reasoning and retrieval, are already proven to address exactly these types of structural limitations. Several of them are training-free and could enhance existing systems today.

The defining open challenge is integrating these geometric foundations into persistent, cross-session memory architectures with evolving graphs. Thank you.

---

## [Discussion]
*~30 seconds*

I would like to open the floor for discussion. Three questions to get us started.

How does your system handle memory that evolves over time? Which structural limitation, multi-hop ceilings, temporal gaps, or semantic collapse, resonates most with your experience? And should geometric representations be built into the memory layer, or should they remain a post-processing step?

I am happy to take any questions.

---
