# Lab 3: Experiencing the Necessity of RAG (Retrieval-Augmented Generation)

## Project Overview
This lab demonstrates the critical limitations of context-free AI responses and proves why **RAG (Retrieval-Augmented Generation)** is mandatory for reliable enterprise use cases. We compared the AI's performance when asked a company-specific question about refund policies and server locations without documents (Baseline) versus with internal documents provided (RAG).

## Lab 3-3: Comparative Analysis (The 5 Criteria)

1. **Accuracy (Factual Correctness):** 
   * *Baseline:* The AI could not provide the actual policy. Instead of hallucinating, it gave generic sales advice (e.g., checking an MSA or SOW).
   * *RAG:* 100% accurate based on the provided context.
2. **Specificity (Concrete Details):** 
   * *Baseline:* Completely vague. It suggested looking at a CRM (Salesforce) or internal Wiki (Notion/Confluence) rather than giving concrete numbers.
   * *RAG:* Highly specific, explicitly mentioning the $49/month cost, the 14-day rule, the 10GB limit, and the Frankfurt servers.
3. **Grounding (Based on Sources):** 
   * *Baseline:* Not grounded in company reality. The AI relied on its pre-trained general knowledge of typical B2B sales workflows.
   * *RAG:* Perfectly grounded. The AI strictly extracted information from "Document A: FlowNote Enterprise Pricing" and "Document B: FlowNote Data Security".
4. **Hallucination Risk:** 
   * *Baseline:* While the model safely admitted it didn't have access to internal databases, in many other scenarios, models attempt to guess company policies, posing a massive hallucination risk.
   * *RAG:* Zero. The prompt strictly constrained the AI to the provided documents with the rule: "If the information is not in the documents, say 'I don't know'."
5. **Trustworthiness (Business Use):** 
   * *Baseline:* Untrustworthy for real business contexts; a sales rep cannot send this AI output to a waiting customer.
   * *RAG:* Highly trustworthy. This approach is safe for deployment in enterprise environments.

## Conclusion & Golden Rule
If a task requires specific, up-to-date, or private organizational knowledge, relying on a general-purpose LLM alone is ineffective. **I will always use the RAG approach** to ground the AI's reasoning in external, verified documents to ensure actionable and factually correct outputs.
