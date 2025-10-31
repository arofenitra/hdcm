# Hallucination detection in LLM coder. 
## Problem Definition and Scope.
### Specific type of hallucination.
They fall usually in one of these class, but we will consider only the first classification.
1. **Logic hallucination VS Ressource hallucination VS Naming hallucination etc**.
2. Fact-conflicting VS Input conflicting VS Context conflicting (conflict with previous code, etc.) 
3. Security hallucination VS Robustness issues
### Reason of the research :  
This example can happen in real world deployement : ```requests.get()``` (retrieve data from a specified URL) $\rightarrow$ ```requests.delete()``` (delete specific ressource from a server). 
### Scope
**Code generator** , code completion, agentic AI.

## Dataset and benchmark selection
List of papers on hallucination detection in LLMs:   

https://github.com/EdinburghNLP/awesome-hallucination-detection


|  | Components | Code | Paper|
| ------------ | ---------- | ------------- | ------- | 
| Core Dataset | **CodeMirage** |https://huggingface.co/datasets/HanxiGuo/CodeMirage| https://www.arxiv.org/pdf/2408.08333|
| Evaluation benchmark | **HaluEval** |https://github.com/RUCAIBox/HaluEval |https://aclanthology.org/2023.emnlp-main.397/|


| Dataset / Benchmark            | Focus / Scope                  | Paper / Source               | Notes                                   |
| ------------------------------ | ------------------------------ | ---------------------------- | --------------------------------------- |
| HaluEval                       | General LLM hallucination      | HaluEval paper & GitHub repo | 35K samples, human and auto-labeled     |
| HalluVerse25                   | Multilingual fine-grained      | arXiv:2503.07833             | English, Arabic, Turkish hallucinations |
| Kaggle ML Olympiad             | Hallucination detection        | https://www.kaggle.com/competitions/ml-olympiad-detect-hallucinations-in-llms           | Challenge dataset                       |
| LLM-Check                      | Synthetic hallucination data   | https://openreview.net/pdf?id=LYx4w3CAgy             | Error injection/Synthetic hallucination |
| RAGAS / RAGAS++                | RAG-specific hallucination     | https://cleanlab.ai/blog/rag-tlm-hallucination-benchmarking/               | Faithfulness, relevance metrics         |
| Code LLMs hallucination        | Taxonomy + benchmarks          | arXiv:2504.20799             | Review of code generation hallucination |
| HSAD                           | Hidden layer spectral features | arXiv:2509.23580             | Frequency domain analysis method        |
| Awesome Hallucination Datasets | Collection and references      | EdinburghNLP GitHub          | Wide range of datasets & benchmarks     |

MBPP/HumanEval : Baseline for functional correctness 
HaluCode - CodeMirage : Dataset that can be used 
## Programming Language and tools 
Python , Rust, Java, Lua
