Dear Michael Banf,

We are happy to inform you that your FGWM 2026 submission 128 entitled:
  "Graph-Structured Memory for Cognitive Agents: From Knowledge Graphs to Non-Euclidean Geometry"
has been accepted for presentation (10 minutes presentation + 5 minutes discussion).

We have attached the reviews for your paper below. Please consider the remarks for the preparation of the camera-ready copy. The camera-ready copy should be ready until 9th of August.

Attached you will find the copyright from for CEUR. Please fill out the form and upload it in addition to the camera-ready copy.

If you have any questions, please write an email to pascalreuss@gmx.de.

With kind regards
Johannes, Lisa & Pascal
(FG-WM Workshop Chairs)

SUBMISSION: 128
TITLE: Graph-Structured Memory for Cognitive Agents: From Knowledge Graphs to Non-Euclidean Geometry

----------------------- REVIEW 1 ---------------------

SUBMISSION: 128
TITLE: Graph-Structured Memory for Cognitive Agents: From Knowledge Graphs to Non-Euclidean Geometry

----------- Overall evaluation -----------
SCORE: 3 (fair)
----- TEXT:
In this paper, the main problem revolves around LLMs needing long-term, cross-session memory that handles time-based changes and complex, multi-hop reasoning. Simply cramming or compressing pastchats into an expanding context window destroys important relational structures.
The presented alternative is storing knowledge in graph structures to allow selective retrieval. However, current systems force these graphs into standard Euclidean space, which distorts hierarchical, tree-like structures natural to agent memory.
This survey highlights six arcitectural patterns and a wide range of retrieval methods. It also analyzes that non-Euclidean geometric techniques outshine Euclidean baselines in data retrieval and knowledge graph reasoning.
The identified challenge is the integration of the techniques into cross.session memory architectures.


For a survey paper in general I would recommend "State-of-the-Art des State-of-the-Art" - Peter Fettke
This paper would benefit from more clear communication on how the literature for the different topics was gathered. This would help with evaluating the scope of this survey.

The presented literature and the identified challenge are sound.


----------------------- REVIEW 2 ---------------------

SUBMISSION: 128
TITLE: Graph-Structured Memory for Cognitive Agents: From Knowledge Graphs to Non-Euclidean Geometry

----------- Overall evaluation -----------
SCORE: 4 (good)
----- TEXT:
This paper surveys recent research on graph-based memory architectures for LLM agents and argues that the next major step in persistent agent memory is the integration of non-Euclidean geometric representations. The authors classify recent graph-memory systems into six architectural categories, analyse their retrieval mechanisms, and identify shortcomings in temporal reasoning and graph retrieval. Building on this survey, they propose that techniques from geometric deep learning—including hyperbolic embeddings, Ricci curvature, Lie group manifolds, and mixed-curvature product spaces—can address current limitations in hierarchical retrieval, temporal reasoning, and graph evolution. The paper concludes with a research agenda for geometry-aware persistent agent memory.

The paper addresses an interesting and relevant research topic. Persistent memory for LLM agents has become one of the most active areas of current AI research, and the attempt to connect graph-based agent memory with advances in geometric representation learning is timely and potentially impactful.

The paper covers a large number of recent systems published between 2023 and 2026 and organizes them into a coherent taxonomy. The comparision between graph representations, temporal mechanisms, retrieval strategies, evolution mechanisms, and benchmark results in a compact overview is very valuable. Likewise, the discussion of retrieval strategies ranging from graph algorithms to learned GNN retrieval provides a useful synthesis of the current landscape. In addition, the conceptual integration of several research areas that are often discussed independently, is very good. The paper successfully connects agent memory, knowledge graphs, geometric deep learning, and temporal knowledge graphs into a unified perspective. The proposed research agenda is well motivated and identifies several meaningful open questions.

The paper is generally well structured and easy to follow. The taxonomy of graph-memory architectures provides a logical narrative, and Figure 1 effectively illustrates the progression from flat memories to geometric representations.

However, the transition from the survey section to the geometric section is somewhat abrupt. In addition, the section on geometric methods introduces many advanced mathematical concepts in rapid succession, making it difficult for readers outside geometric deep learning.

The discussion would benefit from one concrete running example showing how an existing graph-memory architecture could be enhanced using one of the proposed geometric techniques.

The distinction between survey results and the authors' own contributions seems an issue regarding the authors contribution. While the paper lists four contributions, much of the content consists of summarizing existing literature. The genuinely novel contribution appears to be the synthesis itself rather than new methodology or empirical findings. This distinction should be made more explicit.

The retrieval analysis remains largely qualitative. Statements such as graph memory "equalizing small models to near-frontier performance" are based on comparisons across different published systems rather than controlled experimental evaluation. Since benchmark settings, datasets, and base models differ substantially, these comparisons should be interpreted more cautiously.

One point for improvement would be to clearly separating survey contributions from original research contributions.


Overall, this paper provides a comprehensive survey of graph-based memory for LLM agents and offers an interesting vision for integrating geometric deep learning into future memory architectures. The literature synthesis is valuable, the taxonomy is well designed, and the proposed research agenda is relevant to the knowledge management community. However, the work is primarily conceptual and lacks experimental validation of its central ideas.


----------------------- REVIEW 3 ---------------------

SUBMISSION: 128
TITLE: Graph-Structured Memory for Cognitive Agents: From Knowledge Graphs to Non-Euclidean Geometry

----------- Overall evaluation -----------
SCORE: 4 (good)
----- TEXT:
The manuscript “Graph-Structured Memory for Cognitive Agents: From Knowledge Graphs to Non-Euclidean Geometry” surveyed research paper between 2023 and 2026 to identify architectural patterns and a retrieval spectrum to graph neural network message passing. While the topic is current and interesting, the manuscript has some potential for improvement. Hence, please consider the following major comments:

Major comments:
1. For research articles, one would expect an IMRD approach so that you argue your introduction, display your methods, show your results and discuss them. Hence, please consider applying the IMRD approach to your study.
2. Please consider providing theoretical and practical implications of your study. Further, please consider providing limitations as well as future research directions.
3. Please consider providing a research aim as well as a research question for your study.
4. As you wrote a full research paper, one would expect that you first present related work that you then discuss using the insights of your study. Hence, please consider presenting related work and a discussion section.