+++
title = 'Thoughts - RAG evaluation'
date = 2025-01-01T14:38:33+02:00
draft = false
type = 'blog'
+++

Recently, I had to create an evaluation pipeline for my RAG app — to be honest, I was assigned this task through a JIRA ticket 😊, so I had to do it.

But I took it serious based on my past experience with a user recommendation system based on Named Entity Recognition (NER) I built, I realized that I hadn’t implemented production metrics. Specifically, I didn’t have a feedback system that could generate an evaluation dataset from production data. 

I could have tracked metrics like click-through rates, and we did have a user manual input option (which was meant to be replaced by the recommender system). This allowed us to observe when users ignored recommendations in favor of the older approach, signaling potential issues with the new one. 

So, I decided to take a step toward better evaluation at least by creating a unit test-like system to monitor my current app whenever I make significant changes—whether that’s modifying the vector database, switching to a new model, or adjusting the system prompt for a specific output format.
During Development, I print query vectors and retrieved context to evaluate the app. Sometimes, I would visualize these vectors to manually assess the similarity. I realized there needs a better evaluation pipeline using measurable metrics like context recall, precision, and model adherence to instructions, perturbations.
So, I Started to use Ragas(https://github.com/explodinggradients/ragas). In the LLM approach, you generate reference answers for sampled questions and then use an LLM to evaluate metrics like context recall, semantic similarity, and faithfulness. I’ve experimented with this using the Llama model (via Ollama) and Azure OpenAI models through LangChain. Additionally, the tool allows you to synthesize test datasets using AI (as long as your data is not sensitive).

Here’s what I’ve observed so far:
Confidence in Releases: I can use this system as a unit test (Maybe in LLMOps) that can provide confidence before a release. 
Inconsistent Metrics: Some metrics, like similarity and factual correctness, weren’t consistent even when using the same evaluation dataset. This is understandable since LLMs, when acting as judges, can vary in responses. In RAG evaluation, perfect accuracy in similarity checks across iterations is challenging.
Cost Considerations: Running evaluations using non-open models can get expensive. The tool makes numerous calls to the model, so there’s a trade-off between using cutting-edge models and open-source alternatives for cost-efficiency.
Evaluation Time: It took around 6 minutes to evaluate even with a small dataset containing just 5 examples. I’m still investigating it.

Overall, this is a promising start, and I’m excited to continue refining the process. I’m curious—what methods do you use for evaluating your systems?
hashtag#RAGEvaluation


Originally posted on my LinkedIn Page https://www.linkedin.com/posts/saravanan-maruthanayakam-199b7712b_github-explodinggradientsragas-supercharge-activity-7278802608272678913-QhOz?utm_source=share&utm_medium=member_desktop