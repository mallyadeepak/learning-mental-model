# Large Language Models (LLM)

> LLMs are neural networks trained on massive text datasets that learn to predict and generate human-like text. They capture statistical patterns of language to understand context, reason, and produce coherent responses across diverse tasks.

## Diagram

![LLM Mental Model Diagram](https://mermaid.ink/img/Zmxvd2NoYXJ0IFRCCiAgY2xhc3NEZWYgY29uY2VwdCBmaWxsOiM0QTkwQTQsc3Ryb2tlOiMyQzVGNkUsc3Ryb2tlLXdpZHRoOjJweCxjb2xvcjojZmZmCiAgY2xhc3NEZWYgcHJvY2VzcyBmaWxsOiM3QjY4QTYsc3Ryb2tlOiM0QTNENkUsc3Ryb2tlLXdpZHRoOjJweCxjb2xvcjojZmZmCiAgY2xhc3NEZWYgZXhhbXBsZSBmaWxsOiM1REFFOEIsc3Ryb2tlOiMzRDdBNUUsc3Ryb2tlLXdpZHRoOjJweCxjb2xvcjojZmZmCiAgY2xhc3NEZWYgYW5hbG9neSBmaWxsOiNENEE1NzQsc3Ryb2tlOiNBNjdCNEEsc3Ryb2tlLXdpZHRoOjJweCxjb2xvcjojZmZmCiAgbGxtKCJMYXJnZSBMYW5ndWFnZSBNb2RlbCIpCiAgdHJhaW5pbmdbIlRyYWluaW5nIl0KICBwcmV0cmFpbmluZ1siUHJlLXRyYWluaW5nIl0KICBmaW5ldHVuaW5nWyJGaW5lLXR1bmluZyAvIFJMSEYiXQogIGFyY2hpdGVjdHVyZSgiQXJjaGl0ZWN0dXJlIikKICB0b2tlbnMoIlRva2VucyIpCiAgYXR0ZW50aW9uKCJBdHRlbnRpb24gTWVjaGFuaXNtIikKICBjYXBhYmlsaXRpZXMoIkNhcGFiaWxpdGllcyIpCiAgcmVhc29uaW5nKFsiUmVhc29uaW5nICYgUUEiXSkKICBnZW5lcmF0aW9uKFsiVGV4dCBHZW5lcmF0aW9uIl0pCiAgbGltaXRhdGlvbnMoIkxpbWl0YXRpb25zIikKICBoYWxsdWNpbmF0aW9uKCJIYWxsdWNpbmF0aW9uIikKICBjb250ZXh0KCJDb250ZXh0IFdpbmRvdyIpCiAgY2xhc3MgbGxtLGFyY2hpdGVjdHVyZSx0b2tlbnMsYXR0ZW50aW9uLGNhcGFiaWxpdGllcyxsaW1pdGF0aW9ucyxoYWxsdWNpbmF0aW9uLGNvbnRleHQgY29uY2VwdAogIGNsYXNzIHRyYWluaW5nLHByZXRyYWluaW5nLGZpbmV0dW5pbmcgcHJvY2VzcwogIGNsYXNzIHJlYXNvbmluZyxnZW5lcmF0aW9uIGV4YW1wbGUKICBwcmV0cmFpbmluZyA9PT58Zm9sbG93ZWQgYnl8IGZpbmV0dW5pbmcKICB0cmFpbmluZyAtLi0-fHNoYXBlc3wgYXJjaGl0ZWN0dXJlCiAgYXR0ZW50aW9uID09PnxlbmFibGVzfCByZWFzb25pbmcKICB0b2tlbnMgPT0-fGlucHV0IHRvfCBhdHRlbnRpb24KICBoYWxsdWNpbmF0aW9uIC0tLXx3b3JzZW5zIGJleW9uZHwgY29udGV4dAoKICBzdWJncmFwaCBMZWdlbmQKICAgIEwxKCJDb25jZXB0Iik6Ojpjb25jZXB0CiAgICBMMlsiUHJvY2VzcyJdOjo6cHJvY2VzcwogICAgTDMoWyJFeGFtcGxlIl0pOjo6ZXhhbXBsZQogICAgTDR7eyJBbmFsb2d5In19Ojo6YW5hbG9neQogIGVuZA==)

## Concepts

- **Large Language Model** [Concept]
  _A neural network with billions of parameters trained to understand and generate text_
  - **Training** [Process]
    _The process of learning from vast text data_
    - **Pre-training** [Process]
      _Self-supervised learning on internet-scale text — predict the next token_
    - **Fine-tuning / RLHF** [Process]
      _Align the model to be helpful, harmless, and honest using human feedback_
  - **Architecture** [Concept]
    _The Transformer — attention-based neural network backbone_
    - **Tokens** [Concept]
      _Words or sub-words — the atomic units of text the model processes_
    - **Attention Mechanism** [Concept]
      _Lets the model weigh relationships between all tokens in context simultaneously_
  - **Capabilities** [Concept]
    _What LLMs can do_
    - **Reasoning & QA** [Example]
      _Answer questions, summarize, explain, solve problems step by step_
    - **Text Generation** [Example]
      _Write code, essays, stories, translations, structured data_
  - **Limitations** [Concept]
    _Known failure modes_
    - **Hallucination** [Concept]
      _Generates plausible-sounding but factually wrong information_
    - **Context Window** [Concept]
      _Finite memory — can only 'see' a limited number of tokens at once_

## Relationships

- **Pre-training** → *followed by* → **Fine-tuning / RLHF**
- **Training** → *shapes* → **Architecture**
- **Attention Mechanism** → *enables* → **Reasoning & QA**
- **Tokens** → *input to* → **Attention Mechanism**
- **Hallucination** → *worsens beyond* → **Context Window**

## Real-World Analogies

### Pre-training ↔ A student reading millions of books

Just as a student absorbs patterns of language, logic, and facts by reading extensively, an LLM learns statistical patterns from vast text — without explicit right/wrong labels, just by predicting what comes next.

### Attention Mechanism ↔ Highlighting key words while reading a complex sentence

When you parse 'The trophy didn't fit in the suitcase because it was too big', you focus attention on the right referent for 'it'. The attention mechanism does the same — dynamically weighing which tokens are most relevant to each other.

### Context Window ↔ A whiteboard that gets erased periodically

A person with only a small whiteboard to work on must erase earlier notes to write new ones. An LLM's context window is its working memory — once text falls outside it, the model has no access to it.

---
*Generated on 2026-03-22*