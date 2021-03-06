<!-- omit in toc -->
# Research Papers Related to Commonsense Knowledge

<!-- omit in toc -->
## TOC
- [1. Keynotes & Workshops](#1-keynotes--workshops)
- [2. Knowledge Base / Benchmark / System](#2-knowledge-base--benchmark--system)
- [3. Knowledge Mining / Extraction / Generation](#3-knowledge-mining--extraction--generation)
  - [3.1. Technique](#31-technique)
  - [3.2. Distillation](#32-distillation)
  - [3.3. Factual Probing](#33-factual-probing)
- [4. Neural Knowledge Graph](#4-neural-knowledge-graph)
- [5. Application](#5-application)
  - [5.1. Boost LMs](#51-boost-lms)
  - [5.2. 3.2 QA](#52-32-qa)
  - [5.3. 3.3 Reasoning](#53-33-reasoning)
- [6. Related Works](#6-related-works)
  - [6.1. OpenIE](#61-openie)
    - [6.1.1. Pipeline](#611-pipeline)
    - [6.1.2. Supervised Method](#612-supervised-method)
    - [6.1.3. Beyond](#613-beyond)
  - [6.2. Semantic Role Labeling](#62-semantic-role-labeling)
  - [6.3. Entity and Relation Extraction](#63-entity-and-relation-extraction)
  - [6.4. Event Extraction](#64-event-extraction)
  - [6.5. 🧲 Prompts](#65--prompts)
  - [6.6. New Paradigm](#66-new-paradigm)

<!-- omit in toc -->
## Scholar

- mpi-inf [[homepage]](https://www.mpi-inf.mpg.de/departments/databases-and-information-systems/research)
  > Commonsense knowledge about object properties, human behavior and general concepts is crucial for robust AI applications. However, automatic acquisition of this knowledge is challenging because of sparseness and bias in online sources.

- AllenAI
  - Niket Tandon [[github]](https://github.com/nikett)
  - Yejin Choi [[homepage]](https://homes.cs.washington.edu/~yejin/)

- usc-isi-i2 [homepage](https://usc-isi-i2.github.io/home/)
  > ISI's Center on Knowledge Graphs research group combines artificial intelligence, the semantic web, and database integration techniques to solve complex information integration problems. We leverage general research techniques across information-intensive disciplines, including medical informatics, geospatial data integration and the social Web.

- Yangqiu Song [[homepage]](https://www.cse.ust.hk/~yqsong/)

---

## 1. Keynotes & Workshops

- COIN: COmmonsense INference in Natural Language Processing.  EMNLP-IJCNLP. 2019. [[link]](https://coinnlp.github.io/)
- Fact Extraction and Verification. EMNLP / FEVER. 2020. [[link]](https://fever.ai/index.html)
- Commonsense Tutorial. ACL. 2020. [[link]](https://homes.cs.washington.edu/~msap/acl2020-commonsense/)
- Common Sense Knowledge Graphs. AAAI. 2020. [[link]](https://usc-isi-i2.github.io/AAAI21workshop/)
- MH2: Commonsense Knowledge Acquisition and Representation. AAAI. 2021. [[link]](https://usc-isi-i2.github.io/AAAI21Tutorial/)
- Commonsense AI: Myth and Truth. ICLR. 2021. [[link]](https://iclr.cc/virtual/2021/invited-talk/3719)
- Information to Wisdom: Commonsense Knowledge Extraction and Compilation. WSDM. 2021. [[link]](https://www.mpi-inf.mpg.de/commonsense-tutorial-wsdm-2021)
- Commonsense Knowledge Acquisition and Reasoning. CCKS: T4. 2021. [[link]](http://sigkg.cn/ccks2021/?page_id=23) [[video]](https://hub.baai.ac.cn/view/11404)

<!-- omit in toc -->
## Notation
- default: Text

- 📷 for Image

- 🎥 for Video

- 🧲 for Prompt

## 2. Knowledge Base / Benchmark / System

- HowNet - a hybrid language and knowledge resource. NLPKE. 2003. [[paper]](https://ieeexplore.ieee.org/document/1276017)
  - OpenHowNet: An Open Sememe-based Lexical Knowledge Base. ArXiv. 2019. [[paper]](https://arxiv.org/abs/1901.09957)
- XLore: A Large-scale English-Chinese Bilingual Knowledge Graph. ISWC. 2013. [[paper]](https://dl.acm.org/doi/abs/10.5555/2874399.2874430)
- ConceptNet 5: A Large Semantic Network for Relational Knowledge. The People's Web Meets NLP. 2013. [[paper]](https://doi.org/10.1007/978-3-642-35085-6_6)
  - ConceptNet 5.5: An Open Multilingual Graph of General Knowledge. AAAI. 2017. [[paper]](https://aaai.org/ocs/index.php/AAAI/AAAI17/paper/view/14972)
- WebChild: Harvesting and Organizing Commonsense Knowledge from the Web. WSDM. 2014. [[paper]](https://dl.acm.org/doi/10.1145/2556195.2556245)
  - Smarter Than You Think: Acquiring Comparative Commonsense from the Web. AAAI. 2014. [[paper]](https://www.aaai.org/ocs/index.php/AAAI/AAAI14/paper/view/8649)
  - Lights, Camera, Action: Knowledge Extraction from Movie Scripts. AAAI. 2015. [[paper]](https://dl.acm.org/doi/10.1145/2740908.2742756)
  - Knowlywood: Mining Activity Knowledge From Hollywood Narratives. CIKM. 2015. [[paper]](https://dl.acm.org/doi/10.1145/2806416.2806583)
  - Commonsense in Parts: Mining Part-Whole Relations from the Web and Image Tags. AAAI. 2016. [[paper]](https://www.aaai.org/ocs/index.php/AAAI/AAAI16/paper/view/12337)
  - WebChild 2.0: Fine-Grained Commonsense Knowledge Distillation. ACL. 2017. [[paper]](https://www.aclweb.org/anthology/P17-4020/)
- Visual Genome: Connecting Language and Vision Using Crowdsourced Dense Image Annotations. Int. J. Comput. Vis. 2017. [[paper]](https://link.springer.com/article/10.1007%2Fs11263-016-0981-7)
- CN-DBpedia: A Never-Ending Chinese Knowledge Extraction System. IEA/AIE. 2017. [[paper]](https://link.springer.com/chapter/10.1007%2F978-3-319-60045-1_44)
  - CN-DBpedia2: An Extraction and Verification Framework for Enriching Chinese Encyclopedia Knowledge Base. Data Intell. 2019. [[paper]](https://doi.org/10.1162/dint_a_00017)
- ATOMIC: An Atlas of Machine Commonsense for If-Then Reasoning. AAAI. 2019. [[paper]](https://doi.org/10.1609/aaai.v33i01.33013027)
  - (Comet-) Atomic 2020: On Symbolic and Neural Commonsense Knowledge Graphs. AAAI. 2021. [[paper]](https://ojs.aaai.org/index.php/AAAI/article/view/16792)
- 🎥 Video2Commonsense: Generating Commonsense Descriptions to Enrich Video Captioning. EMNLP. 2020. [[paper]](https://doi.org/10.18653/v1/2020.emnlp-main.61)
- 🎥 A Benchmark for Structured Procedural Knowledge Extraction from Cooking Videos. Arxiv. 2020. [[paper]](https://arxiv.org/abs/2005.00706) [[github]](https://github.com/frankxu2004/cooking-procedural-extraction)
- 🎥 **[VidSRL]** Visual Semantic Role Labeling for Video Understanding. CVPR. 2021. [[paper]](https://openaccess.thecvf.com/content/CVPR2021/html/Sadhu_Visual_Semantic_Role_Labeling_for_Video_Understanding_CVPR_2021_paper.html)

## 3. Knowledge Mining / Extraction / Generation

### 3.1. Technique
- **[NEIL]** NEIL: Extracting Visual Knowledge from Web Data. ICCV. 2013. [[paper]](https://ieeexplore.ieee.org/document/6751285)
- Automatic Extraction of Commonsense LocatedNear Knowledge. ACL. 2018. [[paper]](https://aclanthology.org/P18-2016/)
- **[Quasimodo]** Commonsense Properties from Query Logs and Question Answering Forums. CIKM. 2019. [[paper]](https://dl.acm.org/doi/10.1145/3357384.3357955)
  - Inside Quasimodo: Exploring Construction and Usage of Commonsense Knowledge. CIKM. 2020 [[paper]](https://dl.acm.org/doi/10.1145/3340531.3417416)
- Causal Knowledge Extraction through Large-Scale Text Mining. AAAI. 2020. [[paper]](https://ojs.aaai.org//index.php/AAAI/article/view/7092)
- 📷 Cross-media Structured Common Space for Multimedia Event Extraction. ACL. 2020. [[paper]](https://doi.org/10.18653/v1/2020.acl-main.230)
- 📷 GAIA: A Fine-grained Multimedia Knowledge Extraction System. ACL. 2020. [[paper]](https://aclanthology.org/2020.acl-demos.11/)[[github]](https://github.com/GAIA-AIDA/aida-integration)
- Mining Verb-Oriented Commonsense Knowledge. ICDE. 2020. [[paper]](https://ieeexplore.ieee.org/document/9101187/)
- CapableOf Reasoning: A Step Towards Commonsense Oracle. SIGIR. 2020. [[paper]](https://dl.acm.org/doi/10.1145/3397271.3401251)
- ASER: A Large-scale Eventuality Knowledge Graph. WWW. 2020. [[paper]](https://dl.acm.org/doi/10.1145/3366423.3380107)
- TransOMCS: From Linguistic Graphs to Commonsense Knowledge. IJCAI. 2020. [[paper]](https://doi.org/10.24963/ijcai.2020/554)
- Causal Knowledge Extraction from Text using Natural Language Inference. AAAI. 2021. [[paper]](https://ojs.aaai.org/index.php/AAAI/article/view/17876)
- Causal Inference of Script Knowledge. EMNLP. 2020. [[paper]](https://aclanthology.org/2020.emnlp-main.612/)
- **[Ascent]** Advanced Semantics for Commonsense Knowledge Extraction. WWW. 2021. [[paper]](https://arxiv.org/abs/2011.00905)

### 3.2. Distillation
- **[DICE]** Joint Reasoning for Multi-Faceted Commonsense Knowledge. AKBC. 2020. [[paper]](https://www.akbc.ws/2020/papers/QnPV72SZVt)
- Commonsense Knowledge in Wikidata. ISWC. 2020. [[paper]](https://arxiv.org/abs/2008.08114)
- Dimensions of Commonsense Knowledge. ArXiv. 2021. [[paper]](https://arxiv.org/abs/2101.04640)
- CSKG: The CommonSense Knowledge Graph. ESWC. 2021. [[paper]](https://arxiv.org/abs/2012.11490)
- Information to Wisdom: Commonsense Knowledge Extraction and Compilation. WSDM. 2021. [[paper]](https://doi.org/10.1145/3437963.3441664)
- DISCOS: Bridging the Gap between Discourse Knowledge and Commonsense Knowledge. WWW. 2021. [[paper]](https://doi.org/10.1145/3442381.3450117)

### 3.3. Factual Probing
- Commonsense Knowledge Mining from Pretrained Models. EMNLP-IJCNLP. 2019. [[paper]](https://aclanthology.org/D19-1109)
- Language Models as Knowledge Bases. EMNLP/IJCNLP. 2019. [[paper]](https://doi.org/10.18653/v1/D19-1250)
- How Can We Know What Language Models Know. TACL. 2020. [[paper]](https://transacl.org/ojs/index.php/tacl/article/view/1983)
- Knowledgeable or Educated Guess? Revisiting Language Models as Knowledge Bases. EMNLP/IJCNLP. 2021. [[paper]](https://doi.org/10.18653/v1/2021.acl-long.146)
- Factual Probing Is [MASK]: Learning vs. Learning to Recall. NAACL. 2021. [[paper]](https://arxiv.org/abs/2104.05240)

## 4. Neural Knowledge Graph
- COMET: Commonsense Transformers for Automatic Knowledge Graph Construction. ACL. 2019. [[paper]](https://doi.org/10.18653/v1/p19-1470) [[github]](https://github.com/atcbosselut/comet-commonsense)
- Commonsense Knowledge Base Completion with Structural and Semantic Context. AAAI. 2020. [[paper]](https://aaai.org/ojs/index.php/AAAI/article/view/5684)
- Inducing Relational Knowledge from BERT. AAAI. 2020. [[paper]](https://aaai.org/ojs/index.php/AAAI/article/view/6242)
- 📷 KM-BART: Knowledge Enhanced Multimodal BART for Visual Commonsense Generation. ACL/IJCNLP. 2021. [[paper]](https://doi.org/10.18653/v1/2021.acl-long.44)
- 📷 PIGLeT: Language Grounding Through Neuro-Symbolic Interaction in a 3D World. ACL/IJCNLP. 2021. [[paper]](https://doi.org/10.18653/v1/2021.acl-long.159)
- Inductive Learning on Commonsense Knowledge Graph Completion. IJCNN. 2021. [[paper]](https://arxiv.org/abs/2009.09263)


## 5. Application

### 5.1. Boost LMs
- Teaching Pretrained Models with Commonsense Reasoning: A Preliminary KB-Based Approach. NeurIPS. 2019. [[paper]](https://arxiv.org/abs/1909.09743)

### 5.2. 3.2 QA

- CosMo: Conditional Seq2Seq-based Mixture Model for Zero-Shot Commonsense Question Answering. COLING. 2020. [[paper]](https://www.aclweb.org/anthology/2020.coling-main.467)
- Dynamic Neuro-Symbolic Knowledge Graph Construction for Zero-shot Commonsense Question Answering. AAAI. 2021. [[paper]](https://ojs.aaai.org/index.php/AAAI/article/view/16625)
- Fusing Context Into Knowledge Graph for Commonsense Question Answering. ACL. 2021. [[paper]](https://arxiv.org/pdf/2012.04808.pdf)
  - Human Parity on CommonsenseQA: Augmenting Self-Attention with External Attention. Arxiv. 2021. [[paper]](https://arxiv.org/pdf/2012.04808.pdf)

### 5.3. 3.3 Reasoning

## 6. Related Works

### 6.1. OpenIE

- Zero-Shot Information Extraction as a Unified Text-to-Triple Translation. Arxiv. 2021. [[paper]](https://arxiv.org/abs/2109.11171)

#### 6.1.1. Pipeline
- **[OpenIE 1.x]** TextRunner: Open Information Extraction on the Web. NAACL. 2007. [[paper]](https://www.aclweb.org/anthology/N07-4013/)
  - The Tradeoffs Between Open and Traditional Relation Extraction. ACL. 2008. [[paper]](https://www.aclweb.org/anthology/P08-1004/)
  - Using Wikipedia to bootstrap open information extraction. SIGMOD. 2008. [[paper]](https://doi.org/10.1145/1519103.1519113)
  - StatSnowball: a statistical approach to extracting entity relationships. WWW. 2009. [[paper]](https://doi.org/10.1145/1526709.1526724)
  - Open information extraction using wikipedia. ACL. 2010. [[paper]](https://www.aclweb.org/anthology/P10-1013/)
- **[OpenIE 2.x; ReVerb]** Identifying Relations for Open Information Extraction. EMNLP. 2011. [[paper]](https://www.aclweb.org/anthology/D11-1142/)
- **[R2A2]** Open Information Extraction: The Second Generation. IJCAI. 2011. [[paper]](https://doi.org/10.5591/978-1-57735-516-8/IJCAI11-012)
- **[OpenIE 3.x; OLLIE]** Open Language Learning for Information Extraction. EMNLP-CoNLL. 2012. [[paper]](https://www.aclweb.org/anthology/D12-1048/)
- Effectiveness and efficiency of open relation extraction. EMNLP. 2013. [[paper]](https://www.aclweb.org/anthology/D13-1043/)
- **[ClausIE]** ClausIE: clause-based open information extraction. WWW. 2013. [[paper]](https://doi.org/10.1145/2488388.2488420)
- **[OpenIE 4.x]** [[github1]](https://github.com/knowitall/openie) [[github2]](https://github.com/allenai/openie-standalone)
  - **[SRLIE]** An Analysis of Open Information Extraction based on Semantic Role Labeling. KCAP. 2011. [[paper]](https://doi.org/10.1145/1999676.1999697)
  - **[RelNoun]** Demonyms and Compound Relational Nouns in Nominal Open IE. NAACL. 2016. [[paper]](https://doi.org/10.18653/v1/w16-1307)
- **[OpenIE 5.x]** [[github]](https://github.com/dair-iitd/OpenIE-standalone)
  - **[BONIE]** Bootstrapping for Numerical Open IE. ACL. 2017. [[paper]](https://doi.org/10.18653/v1/P17-2050)
  - **[CALMIE]** Open Information Extraction from Conjunctive Sentences. COLING. 2018. [[paper]](https://aclanthology.org/C18-1194/)
- **[MinIE]** MinIE: Minimizing Facts in Open Information Extraction". EMNLP. 2017. [[paper]](https://aclanthology.org/D17-1278/)
- **[StuffIE]** StuffIE: Semantic Tagging of Unlabeled Facets Using Fine-Grained Information Extraction. CIKM. 2018. [[paper]](https://dl.acm.org/doi/abs/10.1145/3269206.3271812)
- Graphene: Semantically-Linked Propositions in Open Information Extraction. COLING. 2018. [[paper]](https://aclanthology.org/C18-1195/)

#### 6.1.2. Supervised Method
- **[RnnOIE; Tag]** Supervised Open Information Extraction. NAACL-HLT. 2018. [[paper]](https://doi.org/10.18653/v1/n18-1081)
- **[CopyAttention; Generation]** Neural Open Information Extraction. ACL. 2018. [[paper]](https://aclanthology.org/P18-2065/)
- **[Seq2Seq; Generation]** Logician: A Unified End-to-End Neural Approach for Open-Domain Information Extraction. WSDM. 2018. [[paper]](https://arxiv.org/abs/1904.12535)
- **[SpanOIE; Span]** Span Model for Open Information Extraction on Accurate Corpus. AAAI. 2020. [[paper]](https://aaai.org/ojs/index.php/AAAI/article/view/6497)
- **[OpenIE 6.x; Tag]** OpenIE6: Iterative Grid Labeling and Coordination Analysis for Open Information Extraction. EMNLP. 2020. [[paper]](https://doi.org/10.18653/v1/2020.emnlp-main.306) [[github]](https://github.com/dair-iitd/openie6)
- **[IMoJIE; Generation]** IMoJIE: Iterative Memory-Based Joint Open Information Extraction. ACL. 2020. [[paper]](https://doi.org/10.18653/v1/2020.acl-main.521)
- **[MacroIE; Tag]** Maximal Clique Based Non-Autoregressive Open Information Extraction. EMNLP. 2021. [[paper]](https://aclanthology.org/2021.emnlp-main.764/)

#### 6.1.3. Beyond
- DocOIE: A Document-level Context-Aware Dataset for OpenIE. ACL-IJCNLP(Findings). 2021. [[paper]](https://aclanthology.org/2021.findings-acl.210/)

### 6.2. Semantic Role Labeling

- Jointly Predicting Predicates and Argumentsin Neural Semantic Role Labeling. ACL. 2018. [[paper]](https://aclanthology.org/P18-2058/)
- Dependency or Span, End-to-End Uniform Semantic Role Labeling. AAAI. 2019. [[paper]](https://doi.org/10.1609/aaai.v33i01.33016730)

### 6.3. Entity and Relation Extraction

- Locate and Label: A Two-stage Identifier for Nested Named Entity Recognition. ACL/IJCNLP. 2020. [[paper]](https://doi.org/10.18653/v1/2021.acl-long.216)
- **[PURE]** A Frustratingly Easy Approach for Entity and Relation Extraction. NAACL-HLT. 2021. [[paper]](https://doi.org/10.18653/v1/2021.naacl-main.5)
- 🧲 Template-Based Named Entity Recognition Using BART. ACL/IJCNLP(Findings). 2021. [[paper]](https://doi.org/10.18653/v1/2021.findings-acl.161)

### 6.4. Event Extraction
- **[OneIE]** A Joint Neural Model for Information Extraction with Global Features. ACL. 2020. [[paper]](https://aclanthology.org/2020.acl-main.713/)
- Text2Event: Controllable Sequence-to-Structure Generation for End-to-end Event Extraction. ACL/IJCNLP. 2021. [[paper]](https://doi.org/10.18653/v1/2021.acl-long.217)
- 🧲 Generating Disentangled Arguments with Prompts: A Simple Event Extraction Framework that Works. Arixv. 2021. [[paper]](https://export.arxiv.org/abs/2110.04525)
- 🧲 Eliciting Knowledge from Language Models for Event Extraction. Arixv. 2021. [[paper]](https://arxiv.org/abs/2109.05190)

### 6.5. 🧲 Prompts
- WARP: Word-level Adversarial ReProgramming. ACL/IJCNLP. 2021. [[paper]](https://doi.org/10.18653/v1/2021.acl-long.381)
- Prefix-Tuning: Optimizing Continuous Prompts for Generation. ACL/IJCNLP. 2021. [[paper]](https://doi.org/10.18653/v1/2021.acl-long.353)
- The Power of Scale for Parameter-Efficient Prompt Tuning. EMNLP. 2021. [[paper]](https://arxiv.org/abs/2104.08691)
- Surface Form Competition: Why the Highest Probability Answer Isn’t Always Right. EMNLP. 2021. [[paper]](https://aclanthology.org/2021.emnlp-main.564)
- **[P-Tuning]** GPT Understands, Too. Arxiv. 2021. [[paper]](https://arxiv.org/abs/2103.10385)
- P-Tuning v2: Prompt Tuning Can Be Comparable to Fine-tuning Universally Across Scales and Tasks. Arxiv. 2021. [[paper]](https://arxiv.org/abs/2110.07602v2)

### 6.6. New Paradigm
- Structured Prediction as Translation between Augmented Natural Languages. ICLR. 2021. [[paper]](https://openreview.net/forum?id=US-TP-xnXI)
- A Unified Generative Framework for Aspect-Based Sentiment Analysis. ACL/IJCNLP. [[paper]](https://aclanthology.org/2021.acl-long.188/)
- A Unified Generative Framework for Various NER Subtasks. ACL/IJCNLP. [[paper]](https://aclanthology.org/2021.acl-long.451/)