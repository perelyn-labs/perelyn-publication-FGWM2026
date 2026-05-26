# MemAgents Workshop @ ICLR 2026 - Paper Index

Total: 70 papers (15 oral, 55 poster)

## [1] Retrieval-Augmented LLM Agents: Learning to Learn from Experience [Poster]
ID: HXTOSwUwF6  
Abstract: While large language models (LLMs) have advanced the development of general-purpose agents, achieving robust generalization to unseen tasks remains a significant challenge. Current approaches typically rely on either fine-tuning or training-free memory-augmented generation using retrieved experience...

## [2] Episodic Memory from Compression Boundaries in Latent Representation Space [Oral]
ID: En9aRT4uz8  
Abstract: Long-term memory in Large Language Model (LLM) agents requires selective persistence: only a subset of interactions should be consolidated beyond the current context window. Existing memory systems rely on heuristic importance rules or similarity-based novelty, which remain external to the model’s i...

## [3] Chow–Liu Ordering for Long-Context Reasoning in Chain-of-Agents [Oral]
ID: krfs16Y8SA  
Abstract: Sequential multi-agent reasoning frameworks such as $\textit{Chain-of-Agents (CoA)}$ handle long-context queries by decomposing inputs into chunks and processing them sequentially using LLM-based worker agents that read from and update a bounded shared memory. From a probabilistic perspective, CoA a...

## [4] Memory Transplants for LLM Agents: Disentangling Architecture and Content Transfer under a Code-to-Math Shift [Poster]
ID: AIJsjIqfsp  
Abstract: Memory-augmented LLM agents accumulate experience to improve over time, but when transferring to a new domain, observed gains may stem from either the memory mechanism (how experiences are stored and retrieved) or the stored content (the experiences themselves). Prior cross-domain evaluations confla...

## [5] Toward a Theory of Hierarchical Memory for Language Agents [Oral]
ID: 8GRnzouMjR  
Abstract: Many recent long-context and agentic systems address context-length limitations by adding hierarchical memory: they extract atomic units from raw data, build multi-level representatives by grouping and compression, and traverse this structure to retrieve content under a token budget. Despite recurri...

## [6] Did You Check the Right Pocket? Cost-Sensitive Store Routing for Memory-Augmented Agents [Poster]
ID: iGRGjdhl9r  
Abstract: Memory-augmented agents maintain multiple specialized stores, yet most systems retrieve from all stores for every query, increasing cost and introducing irrelevant context. We formulate memory retrieval as a store-routing problem and evaluate it using coverage, exact match, and token efficiency metr...

## [7] Compute Allocation for Reasoning-Intensive Retrieval Agents [Poster]
ID: nqr4eTODKl  
Abstract: As agents operate over long horizons, their memory stores grow continuously, making retrieval critical to accessing relevant information. Many agent queries require reasoning-intensive retrieval, where the connection between query and relevant documents is implicit and requires inference to bridge. ...

## [8] SelfEvoWM:Self-Evolving Task Discovery and In-Imagination Robot Learning with DROID-Grounded World Models [Poster]
ID: lVn5vLOkjP  
Abstract: Controllable generative world models make it possible to iterate on manipulation behaviors without repeatedly running real robots. In practice, the bottleneck is often not only ``how to generate'' but how to keep an automated loop tethered to the same assumptions that make classical simulation pipel...

## [9] Norm-Guided KV-Cache Eviction for Memory-Efficient Reasoning [Poster]
ID: xOW2jXDKG3  
Abstract: Large language models deployed as autonomous agents face a fundamental memory
constraint: the KV-cache required for autoregressive generation scales
quadratically with context length. We propose \textbf{$\ell_2$-Norm Eviction},
a novel gradient-free KV-cache compression method that scores tokens by ...

## [10] Diagnosing Retrieval vs. Utilization Bottlenecks in LLM Agent Memory [Poster]
ID: cxYbqAtBIz  
Abstract: Memory-augmented LLM agents store and retrieve information from prior interactions, yet the relative importance of how memories are written versus how they are retrieved remains unclear. We introduce a diagnostic framework that analyzes how performance differences manifest across write strategies, r...

## [11] R-KVHash: Reasoning Model KV Cache Compression Via SimHash-based Estimation of Redundant Tokens [Poster]
ID: UTRuEFJ57H  
Abstract: Reasoning models excel on benchmarks which benefit from multi-step reasoning. However, these reasoning traces are often excessively verbose, producing outputs that contain tens-of-thousands of tokens. The resulting key-value (KV) cache, which stores past token embeddings, grows linearly with sequenc...

## [12] From Storage to Experience: A Survey on the Evolution of LLM Agent Memory Mechanisms [Poster]
ID: l9Ly41xxPb  
Abstract: Large Language Model (LLM)-based agents have fundamentally reshaped artificial intelligence by integrating external tools and planning capabilities. While memory mechanisms have emerged as the architectural cornerstone of these systems, current research remains fragmented, oscillating between operat...

## [13] SuperIntelligent Retrieval Agent: The Next Frontier of Information Retrieval [Poster]
ID: CzzeLatTnI  
Abstract: Retrieval-augmented agents are increasingly the interface to large organizational knowledge bases, yet most treat retrieval as a black box: they can rewrite queries and react to returned snippets, but they cannot directly steer retrieval (e.g., enforce constraints, weight keywords, or decompose quer...

## [14] Experiential Reflective Learning for Self-Improving LLM Agents [Poster]
ID: hQgSl6kj1W  
Abstract: Recent advances in large language models (LLMs) have enabled the development of autonomous agents capable of complex reasoning and multi-step problem solving. However, these agents struggle to adapt to specialized environments and do not leverage past interactions, approaching each new task from scr...

## [15] LP-RAG: A Link Prediction-Based Framework for Retrieval-Augmented Generation [Poster]
ID: Y8Txo8vaH7  
Abstract: Retrieval-augmented generation (RAG) strategies have empowered large language models (LLMs) through integration with external knowledge sources, thereby enabling more accurate, up-to-date, and contextually relevant outputs. Among these, graph-based RAG methods stand out as particularly prominent. Th...

## [16] Log-Augmented Generation: Scaling Test-Time Reasoning with Reusable Computation [Oral]
ID: tn8umfh5X0  
Abstract: While humans naturally learn and adapt from past experiences, large language models (LLMs) and their agentic counterparts often fail to retain reasoning from previous tasks and apply it to future contexts.
We introduce **L**og-**A**ugmented **G**eneration (LAG), a novel framework that *directly reus...

## [17] Spectral Attention Steering for Prompt Highlighting [Oral]
ID: HAmQ65v22N  
Abstract: Steering a large language model's attention towards user-specified highlighted text is a critical capability. Existing prompt highlighting methods are incompatible with modern efficient attention mechanisms like Flash Attention due to their reliance on post-hoc matrix editing. We introduce Spectral ...

## [18] SABER: Small Actions, Big Errors — Safeguarding Mutating Steps in LLM Agents [Poster]
ID: En2z9dckgP  
Abstract: Despite rapid progress in LLM agents, performance on long-horizon, tool-using tasks remains fragile. To better understand this fragility, we ask a simple question: do all actions contribute equally to failure? Analyzing execution traces on $\tau$-Bench (Airline/Retail) and SWE-Bench Verified, we dec...

## [19] PROCED-MEM: BENCHMARKING PROCEDURAL MEMORY RETRIEVAL IN LANGUAGE AGENTS ACROSS DOMAINS [Poster]
ID: 4YhU3BZgoZ  
Abstract: We introduce Proced-Mem, a benchmark for procedural memory retrieval in language agents with two sub-domains: text-based household tasks (ALFWorld) and real computer environments (OSWorld). Evaluating retrieval independently of downstream execution is critical because current agent evaluations confl...

## [20] ShiftBench: Measuring Recovery of Agent Memory Under Distribution Shift [Poster]
ID: CCSztIjmOy  
Abstract: Selecting memory policies by long-horizon accuracy can be misleading under shift, because rankings may reverse when evaluated by post-shift recovery. We introduce ShiftBench, a lightweight protocol defining shift segments and Recovery@T on LoCoMo and HaluMem-Long. On LoCoMo, lexical baselines (TF--I...

## [21] Multi-Agent Collaborative Framework for Intelligent IT Operations: An AOI System with Context-Aware Compression and Dynamic Task Scheduling [Poster]
ID: Q16XXJou3O  
Abstract: The proliferation of cloud-native architectures, characterized by microservices and dynamic orchestration, has rendered modern IT infrastructures increasingly complex and volatile. This complexity generates overwhelming volumes of operational data, creating critical bottlenecks in information proces...

## [22] Tool use is provably more scalable than in-weight memory for Large Language Models [Poster]
ID: s7IRNX6FUs  
Abstract: Tool-augmented language models, equipped with retrieval, memory, or external APIs, are reshaping AI. Yet,
their theoretical advantages remain underexplored. In this paper, we address this question by demonstrating
the benefits of *in-tool learning* (external retrieval) over*in-weight learning* (memo...

## [23] MemGrad: A Memory-Guided Optimization of Agentic Software Development via Abstracted Textual Gradients [Poster]
ID: GeaPE7iw1V  
Abstract: Agentic systems built on large language models increasingly operate in settings that demand stable reasoning, effective collaboration, and reliable adaptation. Existing optimization methods offer valuable signals through prompting strategies, alignment techniques, decentralized coordination, and exp...

## [24] INFMEM: Learning System-2 Memory Control for Long-Context Agent [Oral]
ID: zJirFEiqem  
Abstract: Reasoning over ultra-long documents requires synthesizing sparse evidence scattered across distant segments under strict memory constraints. While streaming agents enable scalable processing, their passive memory update strategy often fails to preserve low-salience bridging evidence required for mul...

## [25] Memory-Efficient Multilingual Embeddings with a Diffusion-LM Backbone [Poster]
ID: QdfiYLNRfB  
Abstract: Dense textual embeddings are essential for web-scale search and retrieval-augmented generation, but their high memory and storage costs limit deployment across billions of documents. We introduce pplx-embed, a family of multilingual text embedding models that employs native quantization-aware traini...

## [26] Evaluating Memory Structure in LLM Agents [Oral]
ID: a9vY2sJkf4  
Abstract: Modern LLM-based agents and chat assistants rely on long-term memory frameworks to store reusable knowledge, recall user preferences, and augment reasoning. As researchers create more complex memory architectures, it becomes increasingly difficult to analyze their capabilities and guide future memor...

## [27] Human-Like Lifelong Memory: A Neuroscience-Grounded Architecture for Infinite Interaction [Poster]
ID: QufkvHbQs7  
Abstract: Large language models lack persistent, structured memory for long-term interaction and context-sensitive retrieval. Expanding context windows does not solve this: recent evidence shows that **context length alone degrades reasoning by up to 85%**—even with perfect retrieval. We propose a bio-inspire...

## [28] Feedback Descent: Open-Ended Text Optimization via Pairwise Comparison [Poster]
ID: Uw5G3H26ps  
Abstract: We introduce Feedback Descent, a framework that optimizes text artifacts through structured textual feedback rather than scalar rewards. At each iteration, an evaluator compares the current best artifact against a new candidate, returning both a preference and a textual rationale explaining why. The...

## [29] FactorMiner: A Self-Evolving Agent with Skills and Experience Memory for Financial Alpha Discovery [Poster]
ID: TTsecyqrW3  
Abstract: Formulaic alpha factor mining is a critical yet challenging task in quantitative investment, characterized by a vast search space and the need for domain-informed, interpretable signals. However, finding novel signals becomes increasingly difficult as the library grows due to high redundancy. We pro...

## [30] Latent Action Reparameterization for Efficient Agent Inference [Poster]
ID: nmFfyHEs76  
Abstract: Large language model (LLM) agents often rely on long sequences of low-level textual actions, resulting in large effective decision horizons and high inference cost. While prior work has focused on improving inference efficiency through system-level optimizations or prompt engineering, we argue that ...

## [31] Do LLMs Benefit From Their Own Words? [Poster]
ID: paoXhcxHgS  
Abstract: In multi-turn conversations, large language models typically condition on the full dialogue transcript: both past user prompts and assistant responses. We revisit this design choice by comparing full-context prompting against three alternative, substantially-reduced context configurations. Analyzing...

## [32] Alleviating Forgetfulness of Linear Attention by Hybrid Sparse Attention and Contextualized Learnable Token Eviction [Poster]
ID: nyJy6R348F  
Abstract: Linear-attention models that compress the entire past memory into a fixed-size recurrent state offer an efficient alternative to Transformers, but the finite memory induces forgetfulness that harms retrieval-intensive scenarios.
To mitigate the issue, we explore a series of hybrid memory architectur...

## [33] Agentic Memory Should Localize Compression [Poster]
ID: ztmwHisqJ4  
Abstract: Long-horizon LLM agents require memory, but unbounded storage is unusable at inference time, making compression unavoidable. In continual deployment, compression becomes repeated updates to accessible state and can induce behavioural drift on previously supported queries. We formalize this as _inter...

## [34] CraniMem: Cranial Inspired Gated and Bounded Memory for Agentic Systems [Poster]
ID: Tts94WVw40  
Abstract: Large language model (LLM) agents are increasingly deployed in long running workflows, where they must preserve user and task state across many turns. Many existing agent memory systems behave like external databases with ad hoc read/write rules, which can yield unstable retention, limited consolida...

## [35] MEMORY IS RECONSTRUCTED, NOT RETRIEVED: GRAPH MEMORY FOR LLM AGENTS [Poster]
ID: YPoHy6lgKP  
Abstract: Despite recent progress, LLM agents still struggle with reasoning over long interaction histories.
While current memory-augmented agents rely on a static ``retrieve-then-reason'' paradigm, this rigid pipeline design prevents them from dynamically adapting memory access to intermediate evidence disco...

## [36] Belief Engine: Bayesian Memory for Configurable Opinion Dynamics in LLM Agents [Poster]
ID: cbkX3XQtip  
Abstract: Large Language Model (LLM) agents can debate fluently, but they do not reliably maintain beliefs across long interactions. This makes it difficult to use them for opinion-dynamics studies where trajectories must be stable, interpretable, and reproducible. We introduce the Belief Engine, a configurab...

## [37] Agentic Context Engineering: Evolving Contexts for Self-Improving Language Models [Oral]
ID: 9EPY8DDQYv  
Abstract: Large language model (LLM) applications such as agents and domain-specific reasoning increasingly rely on *context adaptation*—modifying inputs with instructions, strategies, or evidence, rather than weight updates. 
Prior approaches improve usability but often suffer from brevity bias, which drops ...

## [38] From Lossy to Verified: A Provenance-Aware Tiered Memory for Agents [Poster]
ID: dJgeY3Awrv  
Abstract: Long-horizon agents often rely on write-time summaries to keep interaction histories manageable. But compression happens before the system knows what a future query will depend on. As a result, summary-only memory can remain topically relevant while omitting the query-critical detail required for a ...

## [39] Learning What to Learn: Curriculum Curation for Test-Time Agent Learning [Poster]
ID: Qr5bhBbBOb  
Abstract: Test-time learning enables large language model (LLM) agents to adapt during inference without costly retraining, yet prior work largely treats test-time experience as equally useful. We ask a simple question: *what data should agents learn from at test time?* Focusing on task selection and ordering...

## [40] CoMem: Context Management with A Decoupled Long-Context Model [Poster]
ID: tc9GAKlxQC  
Abstract: Context management enables agentic models to solve long-horizon tasks through iterative summarization of previous interaction histories. However, this process typically incurs substantial decoding overhead for the extra summarization tokens, which significantly affect the end-to-end response latency...

## [41] Fast-Write, Deep-Read: EcphoryRAG as Dynamic Associative Memory for Lifelong Agents [Poster]
ID: YHSoIbQWR8  
Abstract: Effective long-term memory is the cornerstone of autonomous agents capable of complex reasoning over extended horizons. However, current retrieval-augmented generation (RAG) systems face a critical trade-off: they are either computationally efficient but logically shallow (dense retrieval), or struc...

## [42] Entropic Memory: A Thermodynamics-Inspired Consolidation Mechanism for Lifelong Agent Learning [Poster]
ID: um6VpjcOtj  
Abstract: Large language model (LLM) agents often degrade over long interaction streams because memory accumulates noisy observations that reduce retrieval quality. We propose Entropic Memory, a two-tier memory consolidation mechanism that periodically transfers information from a hot working buffer into a co...

## [43] Learning Safe Robot Planning from Unsafe Experiences: An Episodic Memory Approach for LLM-based Agents [Poster]
ID: KrmyJtyE6k  
Abstract: LLM-based robotic agents can generate unsafe commands that harm humans, objects, or the environment. We propose an episodic safety memory system that learns to filter harmful instructions by storing and retrieving past violation experiences. Our memory architecture maintains episodic stores of unsaf...

## [44] WebCoach: Self-Evolving Web Agents with Cross-Session Memory Guidance [Poster]
ID: FDrGfjwQM5  
Abstract: Multimodal LLM-powered agents have recently demonstrated impressive capabilities in web navigation, enabling agents to complete complex browsing tasks across diverse domains. However, current agents struggle with repetitive errors and lack the ability to learn from past experiences across sessions, ...

## [45] LaCy: What Small Language Models Can and Should Learn into Limited Parametric Memory [Poster]
ID: OK8yNPxQgZ  
Abstract: Language models have consistently grown to compress more world knowledge into their parametric memory, but the knowledge that can be pretrained into them is upper-bounded by their parameter size. Especially the capacity of Small Language Models (SLMs) is limited, leading to factually incorrect gener...

## [46] Learning Multimodal Trajectory Representations for Web Agent Planning [Poster]
ID: XZputtLpjz  
Abstract: Trajectory data, capturing multimodal human actions and states, are pivotal for building autonomous Web agents and transferring skills across tasks, encoding knowledge by compressing past experience into structured Markov sequences. Yet current methods for trajectory modeling remain fragmented, ofte...

## [47] ENGRAM: Effective, Lightweight Memory Orchestration for Conversational Agents [Poster]
ID: qajz4UkgIw  
Abstract: Large language models (LLMs) deployed in user-facing applications require long-horizon consistency: the capacity to remember prior interactions, respect user preferences, and ground reasoning in past events. However, contemporary memory systems often adopt complex architectures such as knowledge gra...

## [48] MIRROR: Complementary Encoding and Reconstructive Consolidation for Persistent State in LLM Systems [Poster]
ID: IviO4bIZc7  
Abstract: LLM-based systems face a fundamental memory consolidation challenge: existing strategies either discard reasoning traces after each turn or accumulate them
unboundedly, trading context preservation against error propagation. Complementary Learning Systems theory suggests a third approach: fast encod...

## [49] Adaptive Memory Admission Control For LLM Agents [Poster]
ID: mmdqUrEY24  
Abstract: LLM-based agents increasingly rely on long-term memory to support multi-session reasoning and interaction, yet current systems provide little control over what information is retained. In practice, agents either accumulate large volumes of conversational content, including hallucinated or obsolete f...

## [50] Learning to Continually Learn via Meta-learning Agentic Memory Designs [Oral]
ID: PRkA1cwXC2  
Abstract: The statelessness of foundation models bottlenecks agentic systems’ ability to continually learn, a core capability for long-horizon reasoning and adaptation. To address this limitation, agentic systems commonly incorporate memory modules to retain and reuse past experience, aiming for continual lea...

## [51] GAM: Hierarchical Graph Memory for LLM-based Agents [Oral]
ID: mmsVZGaYyp  
Abstract: To sustain coherent long-term interactions, Large Language Model (LLM) agents must navigate the tension between acquiring new information and retaining prior knowledge.
Current unified stream-based memory systems facilitate context updates but remain vulnerable to interference from transient noise. ...

## [52] Epistemic Memory Failures in Long-Form Narrative Agents: A Deployment Study [Poster]
ID: u5VS0Eg9DO  
Abstract: We report findings from deploying an LLM-based narrative agent across 90 chapters of novel generation (180,000+ tokens over 3 months). We identify a previously under-discussed failure mode: known-information forgetting---where characters redundantly ask about or rediscover facts they already learned...

## [53] LLMs Can't Play Hangman: On the Necessity of a Private Working Memory for Language Agents [Poster]
ID: AiDSgIwVqL  
Abstract: As LLMs move from text completion toward autonomous agents, they remain constrained by the standard chat interface, which lacks private working memory. This raises a fundamental question: can agents reliably perform interactive tasks that depend on hidden state? We define Private State Interactive T...

## [54] MemoGraph: Augmenting LLMs with Explicit Episodic Memory for Multi-step Mathematical Reasoning [Poster]
ID: HaCqQlEjCN  
Abstract: Large Language Models (LLMs) fundamentally struggle with complex mathematical reasoning due to the volatility of their implicit parametric memory, which leads to context drift and hallucination. Existing paradigms, relying on linear generation or static retrieval, fail to maintain a precise, persist...

## [55] Evaluating AGENTS.md: Are Repository-Level Context Files Helpful for Coding Agents? [Oral]
ID: pLi3A8bscP  
Abstract: A widespread practice in software development is to tailor coding agents
to repositories using context files, such as `AGENTS.md`, by either
manually or automatically generating them. Although this practice is
strongly encouraged by agent developers, there is currently no rigorous
investigation into...

## [56] UltRAG: A universal simple scalable recipe for knowledge graph RAG [Poster]
ID: yN7OBR5lkV  
Abstract: Large language models (LLMs) frequently generate confident yet factually incorrect content when used for language generation (a phenomenon often known as _hallucination_). Retrieval augmented generation (RAG) tries to reduce factual errors by identifying information in a knowledge corpus and putting...

## [57] CloneMem: Benchmarking Long-Term Memory for AI Clones [Poster]
ID: iC2umYHSKW  
Abstract: AI Clones aim to simulate an individual’s thoughts and behaviors to enable long-term, personalized interaction, placing stringent demands on memory systems to model experiences, emotions, and opinions over time. Existing memory benchmarks primarily rely on user–agent conversational histories, which ...

## [58] CAOTE: Optimizing KV Cache Memory Through Attention Output Error-based Token Eviction [Poster]
ID: yolbP0NoZv  
Abstract: Long‑context support in large language models (LLMs) amplifies memory and compute bottlenecks during inference, especially in resource‑constrained environments. A major contributor is the key–value (KV) cache, which grows linearly with sequence length and can exceed model size. Token eviction—removi...

## [59] AMA-Bench: Evaluating Long-Horizon Memory for Agentic Applications [Oral]
ID: GoSVL7mLcM  
Abstract: Large Language Models (LLMs) are deployed as autonomous agents in increasingly complex applications, where enabling long horizon memory is critical for achieving strong performance. However, a significant gap exists between practical applications and current evaluation standards for agent memory: ex...

## [60] Memory Injection Attacks on LLM Agents via Query-Only Interaction [Poster]
ID: i7J62t2wtV  
Abstract: Agents powered by large language models (LLMs) have demonstrated strong capabilities in a wide range of complex, real-world applications. However, LLM agents with a compromised memory bank may easily produce harmful outputs when the past records retrieved for demonstration are malicious. In this pap...

## [61] A Lightweight, Domain-Adaptive Memory System for LLM Agents [Poster]
ID: PLkhOUxkHQ  
Abstract: Long-term memory helps LLM agents solve tasks that require reasoning over long interaction histories. Recent agentic memory systems can outperform providing the full context window or standard retrieval over text chunks, but they often rely on heavy, task-specific context engineering and complex mem...

## [62] MemFly: On-the-Fly Memory Optimization via Information Bottleneck [Poster]
ID: udAdzc3rx9  
Abstract: Long-term memory enables large language model agents to tackle complex tasks through historical interactions. However, existing frameworks encounter a fundamental dilemma between compressing redundant information efficiently and maintaining precise retrieval for downstream tasks. To bridge this gap,...

## [63] ATOD: An Evaluation Framework and Benchmark for Agentic Task-Oriented Dialogue Systems [Poster]
ID: 1L7cY1x2zp  
Abstract: Recent advances in task-oriented dialogue (TOD) systems, driven by LLMs with extensive API and tool integration, have expanded the scope of conversational agents beyond traditional turn-by-turn task execution. Modern systems are increasingly expected to coordinate interleaved goals, preserve long-ho...

## [64] Look Before You Leap: Thermodynamic Arbitration of  Parametric and Non-Parametric Knowledge in LLM Agents via Self-Regulating Memory Architectures [Poster]
ID: w9kwK5Xzvb  
Abstract: The architecture of modern LLMs consists of one profound cognitive polarization. LLMs have an intuition (implicitly) in the vast range of their parameters, yet rely on a disconnected, explicit mechanism to reach the outside world. We have not managed to bridge this gap using agentic frameworks, wher...

## [65] SkillRL: Evolving Agents via Recursive Skill-Augmented Reinforcement Learning [Oral]
ID: By7Pj576U3  
Abstract: Large Language Model (LLM) agents have shown stunning results in complex tasks, yet they often operate in isolation, failing to learn from past experiences. Existing memory-based methods primarily store raw trajectories, which are often redundant and noise-heavy. This prevents agents from extracting...

## [66] Just-In-Time Reinforcement Learning: Continual Learning in LLM Agents Without Gradient Updates [Oral]
ID: us2YPNouOm  
Abstract: While Large Language Model (LLM) agents excel at general tasks, they inherently struggle with continual adaptation due to the frozen weights after deployment. Conventional reinforcement learning (RL) offers a solution but incurs prohibitive computational costs and the risk of catastrophic forgetting...

## [67] Real-Time Procedural Learning From Experience for AI Agents [Poster]
ID: HLuPQ0G1do  
Abstract: Learning how to do things from trial and error in real time is a hallmark of biological intelligence, yet most LLM-based agents lack mechanisms to acquire procedural knowledge after deployment. We propose Procedural Recall for Agents with eXperiences Indexed by State (PRAXIS), a lightweight post-tra...

## [68] DialSim: A Dialogue Simulator for Evaluating Long-Term Multi-Party Dialogue Understanding of Conversational Agents [Poster]
ID: jysCqv1y8O  
Abstract: Recent advancements in Large Language Models (LLMs) have significantly enhanced conversational agents, making them applicable to various fields (e.g., education, entertainment). Despite their progress, the evaluation of the agents often overlooks the complexities of real-world conversations, such as...

## [69] SimpleMem: Efficient Lifelong Memory for LLM Agents [Oral]
ID: CMveUVer0m  
Abstract: To support reliable long-term interaction in complex environments, LLM agents require memory systems that efficiently manage historical experiences. Existing approaches either retain full interaction histories via passive context extension, leading to substantial redundancy, or rely on iterative rea...

## [70] Distilling Feedback into Memory-as-a-Tool [Poster]
ID: hvfhz64q0O  
Abstract: We propose a framework that amortizes the cost of inference-time reasoning by converting transient critiques into retrievable guidelines, through a file-based memory system and agent-controlled tool calls. We evaluate this method on the Rubric Feedback Bench, a novel dataset for rubric-based learnin...

