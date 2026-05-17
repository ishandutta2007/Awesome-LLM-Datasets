# Awesome-LLM-Datasets

## Top LLM Training Datasets Ecosystem

**Curated List of Open Datasets & Data Sources**  
*Focused on High-Quality Datasets for Training Large Language Models*  
**Last updated: March 2026**

This repository tracks the **top open datasets** used for training, fine-tuning, and evaluating Large Language Models (LLMs). These datasets provide massive-scale web data, code, books, scientific papers, conversations, and curated text essential for pre-training and post-training modern LLMs.

**Examples** include FineWeb, The Stack v2, C4 (Colossal Clean Crawled Corpus), RedPajama, Dolma, OSCAR, and The Pile. The focus is strictly on datasets designed or heavily used for building LLMs — emphasizing scale, diversity, cleanliness, and open availability.

**Open data emphasis**: This section is heavily expanded with direct links to Hugging Face, GitHub, and official sources. All datasets listed are openly accessible (or have open versions) for research and commercial use where permitted.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sources.

## Table of Contents
- [Major Data Sources & Collections](#major-data-sources--collections)
- [Open LLM Training Datasets](#open-llm-training-datasets)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## Major Data Sources & Collections

- **[Common Crawl](https://commoncrawl.org/)**  
  The foundational web crawl dataset used by nearly all major LLMs. Massive monthly archives of raw web data.

- **[Hugging Face Datasets Hub](https://huggingface.co/datasets)**  
  Largest open repository hosting processed versions of C4, FineWeb, The Stack, and thousands of LLM-specific datasets.

- **[AllenAI Dolma](https://huggingface.co/datasets/allenai/dolma)**  
  Curated open dataset from AllenAI used in OLMo training.

- **[The Pile](https://huggingface.co/datasets/EleutherAI/pile)**  
  Classic 800GB+ diverse dataset used in many open-source LLMs.

## Open LLM Training Datasets

### Web & General Text Datasets

- **[FineWeb](https://huggingface.co/datasets/HuggingFaceFW/fineweb)**  
  Extremely high-quality cleaned web dataset from Hugging Face. One of the best current open web corpora for LLM pre-training.

- **[C4 (Colossal Clean Crawled Corpus)](https://huggingface.co/datasets/allenai/c4)**  
  Classic cleaned Common Crawl dataset used in T5 and many other models.

- **[C4 (TensorFlow version)](https://www.tensorflow.org/datasets/catalog/c4)**  
  Original TensorFlow Datasets implementation of C4.

- **[OSCAR (Open Super-large Crawled Aggregated coRpus)](https://huggingface.co/datasets/oscar-corpus/OSCAR-2301)**  
  Multilingual web dataset extracted from Common Crawl in over 150 languages.

- **[RedPajama](https://huggingface.co/datasets/togethercomputer/RedPajama-Data-V2)**  
  Open reproduction of LLaMA’s training data with web, books, code, and scientific content.

- **[Dolma](https://huggingface.co/datasets/allenai/dolma)**  
  Massive open dataset (3+ trillion tokens) used to train OLMo, with excellent documentation and provenance.

- **[RefinedWeb](https://huggingface.co/datasets/tiiuae/falcon-refinedweb)**  
  High-quality filtered web data used for Falcon models.

### Code Datasets

- **[The Stack v2](https://huggingface.co/datasets/bigcode/the-stack-v2)**  
  Largest open-source code dataset with permissive licenses across 600+ programming languages.

- **[The Stack Smol](https://huggingface.co/datasets/bigcode/the-stack-smol)**  
  Smaller, high-quality subset of The Stack optimized for efficient training.

- **[StarCoder Data](https://huggingface.co/datasets/bigcode/starcoderdata)**  
  Curated code dataset used for StarCoder models.

### Instruction & Chat Datasets

- **[Prompts.Chat](https://huggingface.co/datasets/fka/prompts.chat)**  
  High-quality instruction-following and chat conversation dataset.

- **[UltraChat](https://huggingface.co/datasets/stingning/ultrachat)**  
  Large-scale multi-turn dialogue dataset for chat model training.

- **[OpenOrca](https://huggingface.co/datasets/Open-Orca/OpenOrca)**  
  High-quality instruction tuning dataset derived from FLAN and other sources.

- **[Tulu 3 / Dolma Conversations](https://huggingface.co/datasets/allenai/tulu-3)**  
  Instruction and preference datasets from AllenAI.

### Specialized & Mixed Datasets

- **[The Pile](https://huggingface.co/datasets/EleutherAI/pile)**  
  Diverse 825GB dataset including web, books, code, academic papers, and more.

- **[BookCorpus2 / Project Gutenberg](https://huggingface.co/datasets/bookcorpus)**  
  Large book datasets used for long-context and narrative understanding.

- **[arXiv Dataset](https://huggingface.co/datasets/arxiv/arxiv)**  
  Scientific papers dataset widely used for technical reasoning capabilities.

- **[PubMed Abstracts](https://huggingface.co/datasets/pubmed)**  
  Biomedical literature dataset for domain-specific knowledge.

- **[Wikipedia (Multiple Languages)](https://huggingface.co/datasets/wikipedia)**  
  Clean, high-quality multilingual encyclopedia data used in almost every LLM.

### Additional High-Value Open Datasets

- **Datatrove** processed Common Crawl subsets (highly filtered versions)
- **SlimPajama** — Cleaned and deduplicated version of RedPajama
- **Proof-Pile** and **MathPile** — Specialized mathematics and reasoning datasets
- **CodeParrot** and other BigCode derivatives
- **mC4** — Massive multilingual version of C4

**Access Tip**: Most datasets above are best accessed via `datasets` library from Hugging Face:
```python
from datasets import load_dataset
dataset = load_dataset("HuggingFaceFW/fineweb", "sample-10BT")