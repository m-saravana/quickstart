+++
title = 'Book Reading- AI Engineering by Chip Huyen'
date = 2024-12-29T19:38:33+02:00
draft = false
type = 'blog'
+++

Just finished reading AI Engineering by Chip Huyen. After reading her earlier book, Designing Machine Learning Systems, I knew I had to dive into this one too. What stands out in both books are her exceptional writing style and the way the chapters are organized. IMHO they can easily serve as handbooks for anyone working with AI and ML. 

The writing is highly relatable to practical use cases, starting with basic concepts and gradually progressing to advanced and contemporary use cases, built on those foundational ideas, with real-world examples of how things have evolved.

Each chapter has foundational concepts and traces their evolution with references to key research papers dating back to the 50s. It’s incredible to think about the depth of research and effort that has gone in entire book. The chapters also highlight improvements, best practices, frameworks, and ongoing research trends.

Here are the topics I particularly enjoyed (All chapters😊):

From Traditional ML Systems to the Rise of Foundation Models: The book delves into the challenges of open-ended outputs, the basics of transformer architecture, key metrics, and real-world business use cases. 

The first two chapters lay a solid foundation for understanding these shifts in AI development.
Model Evaluation: The book covers evaluation at multiple levels, catering to model developers and downstream application developers. Techniques such as iterative evaluation pipelines are explored in detail.

**Prompt Engineering**: A guide on how to write better prompts, advising to start with model providers’ prompt templates, followed by iterations, evaluation, and debugging of prompt metrics.

RAG (Retrieval-Augmented Generation): Using hybrid search with Elastic Search/BM and embedding search is another insightful section that I found especially relevant.

Agents: The book explores when to use agents and when not to after RAG or better prompting, also showing how they evolve naturally from software engineering principles such as function calling. It also discusses common software principles for managing multiple agents, such as using wrappers, frameworks, and tools selection to ensure proper coordination.

Fine-tuning: Detailed discussions on modern fine-tuning techniques. It includes general methods available to frameworks available.

Scaling: A continuous theme throughout the book, scaling strategies are explored with a focus on inference service, model parallelization, and infrastructure/pipeline parallelization. Touching quantization, distillation, and compression are accompanied by helpful diagrams and references.

I intentionally left out many important topics because, honestly, when reading this book, I found myself wondering how I could possibly remember all the insights and recommendations shared (and linked in context limit too). My notes alone are about 50 pages! Every line felt like gold, and I can already see how this knowledge is influencing my day-to-day work with LLMs.


Originally posted on my LinkedIn Page https://www.linkedin.com/posts/saravanan-maruthanayakam-199b7712b_just-finished-reading-ai-engineering-by-chip-activity-7275931342159101952-NJ39?utm_source=share&utm_medium=member_desktop