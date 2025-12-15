# Why use Markdown in your Agents’ System Prompt?

Data Science | Generative AI | Agentic AI | IA | ML

## 💡 Introduction

In the era of AI Agents, one of the most important topics is Prompt Engineering. Basically, Prompt Engineering deals with techniques for building highly efficient prompts, which are essential for creating AI Agents with optimal performance, token savings, and consistent responses.

If you are unfamiliar with the topic, I recommend reading this document from Amazon, which provides an excellent introduction and presents all the related concepts.

### 🎯 Purpose of this article

This article will present some studies that support the claim that the use of structured formats, especially Markdown, offers advantages over plain text and other structured formats, such as HTML, XML, and JSON.

The objective is to raise awareness about the importance of structuring the prompt, especially the System Prompt, in addition to providing the necessary theoretical basis for other works and to defend the use of this technique in your work environment.

### 🔥 Motivation: Consequences of a bad prompt

A poorly structured prompt results in an inefficient, expensive agent that produces poor, inconsistent responses that do not adhere to the instructions provided to the LLM model.

For this reason, many researchers have dedicated themselves to the topic, conducting experiments that prove the advantages of using structured formats for constructing prompts, such as JSON and Markdown.

## 📝 Paper 1: The Prompt Report: A Systematic Survey of Prompt Engineering Techniques

This paper, from February 2025, accessible at this link, is one of the most comprehensive reviews in the field of Prompt Engineering for generative AI. It compiles a vocabulary of 33 terms, offers a taxonomy of 58 prompting techniques for LLMs and 40 techniques for other modalities.

In addition, the paper presents best practices and guidelines for the most advanced language models on the market, such as Chat GPT. It is highly recommended reading for anyone who wants to delve deeper into the subject.

The paper provides scientific and practical validation regarding the use of Markdown for system prompts, presenting the technique as advantageous in terms of clarity, organization, and the model’s ability to follow multi-step instructions with complex examples.

However, the paper does not present experiments that allow for the measurement of specific efficiency (tokens or performance). In this paper, the recommendation is based on a meta-analysis of practices, community reports, and qualitative observations. Further on, however, other sources used in this article will fill this initial gap.

### 📈 Growing use of structured formats

The research documented in the paper recognizes the growing use of structured formats, including Markdown, in prompt engineering. It reinforces that this practice helps in the “logical segmentation” of input, improving readability for humans and also for the model.

The use of Markdown, as a technique for formatting the System Prompt, is cited among the recommended strategies for structuring instructions about the agent’s role, rules to be followed by it, and examples in the input.

### ✅ Advantages of Markdown

Markdown improves the organization, clarity, and interpretability of prompt instructions, which has the potential to increase the overall quality of responses, especially for complex prompts that have multiple topics, functions, or chained examples.

> Formatting prompts using Markdown or similar lightweight markup offers a human-readable structure that supports hierarchical organization (e.g., via headings, bullet points, code blocks) and mitigates ambiguity in multi-step instructions. (Section 3.3, Prompt Structure and Formatting, p.14)

Regarding the use of Markdown formatting for System Prompts, the article states that:

> All experiment protocols and best-practice templates provided in this survey recommend using Markdown headers and bullet points for improving prompt clarity and explicitness. (Table 3, System Prompt Best Practices, p.16)

### 💰 Token savings and efficiency

Although it does not present quantitative benchmarks regarding token savings or efficiency gains, the paper reinforces the use of Markdown as a standard in advanced prompt engineering projects by the professional community.

This practice is highlighted as a technique that leads to greater control over the agent and its compliance with the instructions provided (System Prompt).

> Overall, Markdown emerges as a de facto standard for prompt formatting in industry and research, credited with facilitating model compliance to complex instructions and human validation of prompt components. (Conclusion, page 34)

## 📝 Paper 2: ReaderLM‑v2: Small Language Model for HTML to Markdown and JSON

This second paper, available at this link, presents technical and experimental evidence highlighting the advantages of using structured formats, such as Markdown and JSON, in language model processing and grounding pipelines.

### 🗜️ Compact prompts and token reduction

According to the paper, Markdown results in more compact documents and reduced token usage compared to JSON and HTML.

> By converting raw and noisy HTML into structured Markdown, we significantly reduce non-informative content and facilitate more efficient tokenization and downstream processing, especially for long-context LLM tasks.

> Empirical tests show Markdown’s more compact representation commonly translates to lower token counts (compared to raw HTML or JSON), supporting cost-effective LLM deployments.

> (Section 3, Model Effectiveness, pages 3–4)

### ⚡ Facilitating multitask learning

The article discusses how Markdown facilitates multitask learning by offering a noise-free representation that is more informative from a structural point of view. This favors information extraction and semantic alignment tasks, which are critical capabilities for grounding LLMs.

> We found that grounding on Markdown not only improves extraction fidelity but also simplifies semantic alignment for multitask settings, as the markup provides explicit segmentation of content, headings, and lists. (Section 4, Training Framework and Objectives, pages 4–5)

As a result, this technique avoids ambiguity, increases clarity, and creates the right setting for responses that are more adherent to System Prompt instructions, with higher overall quality.

### ⚡ Improvements in readability and syntactic consistency

The article concludes that the use of Markdown improves readability, syntactic consistency, and compatibility between models, especially in contexts of textual data extraction and preparation for generative AI-based applications.

> Overall, the transition to Markdown yields improvements in both readability and syntactic consistency, which are beneficial for alignment between small document extractors and large LLMs. The format’s broad compatibility also makes it a natural fit for multi-stage pipelines with generative or discriminative models. (Discussion and Conclusion, pages 7–8)

### ✅ Recommendation for using Markdown

As noted, the use of Markdown was evaluated and advocated by the authors of the paper, both from the perspective of experimental performance and practical benefits for readability, structure, and economy in the context of large-scale generative AI.

## 📝 Paper 3: Does Prompt Formatting Have Any Impact on LLM Performance?

The paper, accessible at this link, examines how different prompt formats, including Markdown, JSON, YAML, and plain text, affect the performance of GPT models, focusing on reasoning, code generation, and translation tasks.

### 💡 Capturing task intent

The article presents Markdown as a structured format whose advantages are the combination of human readability with a clear hierarchy.

According to the article, this allows the model to better capture the intent of the task. It also highlights that the use of Markdown has the potential to improve both the organization of information and the model’s interpretation of context.

> Markdown prompt templates leverage lightweight markup syntax to introduce hierarchical structure and improve readability for both humans and models. This enables models to better parse multi-step instructions and distinguish between examples, comments, and directives within the prompt. (Section 3.2, Prompt Templates, page 3)

### ⚖️ Balance between flexibility and structure

The Markdown format is noted as a format that balances flexibility and structure, benefiting complex tasks.

> Markdown is chosen as an intermediate format that balances expressivity and strictness, offering a more organized prompt than plain text but avoiding the verbosity and rigidity of JSON or YAML. (Section 4.1, Experimental Setup, page 4)

### 🧘 Fidelity to instructions

The results of the experiments show that the GPT-3.5-turbo model, for example, shows up to a 40% variation in performance in code translation tasks, depending on the prompt format. In this context, Markdown is one of the best performing formats.

The paper suggests that Markdown helps the model follow context and multiple examples with greater fidelity, avoiding ambiguities and frequent errors that occur with more rigid formats.

> We observe that GPT-3.5-turbo’s code translation accuracy varies by up to 40% depending on the prompt format. Markdown prompts consistently outperform plain text and JSON in most tasks, likely due to improved clarity and structural cues that help the model follow complex instructions. (Section 5.2, Results and Discussion, pages 6–8)

### 🔍 Greater readability

The conclusion of the article highlights the excellent readability of the Markdown format and the resulting improvement in understanding the model.

Markdown emerges as a strong candidate for prompt formatting due to its readability, ease of authoring, and effective preservation of structure, which enhances model understanding and performance on reasoning and generation tasks. (Conclusion, page 10)

### 🎯 Paper Conclusion

The paper confirms, through experiments, that Markdown is a format that combines clarity, efficiency, and robustness for LLMs, improving the quality of outputs in various tasks.

## 👥 Community and Other References

This OpenAI community thread (2024) indicates that Markdown typically consumes about 15% fewer tokens than JSON in LLM prompts and responses, improving performance and computational cost.

The article MDEval: Evaluating and Enhancing Markdown Awareness in Large Language Models directly addresses the issues of efficiency, quality, and clarity in the use of Markdown for prompts in LLMs, but analyzes the use of Markdown in data output. The document reaches conclusions very similar to other sources presented here, namely that the use of Markdown increases overall efficiency and saves tokens compared to other structured data formats.

## 🎯 Conclusion

Several recent sources, experimenting with different ML models, confirm that the use of structured formats, especially Markdown, offers many advantages when applied to the System Prompt of Generative AI Agents using LLM models.

Among the main advantages are:

1. Improves the organization, clarity, and interpretability of prompt instructions (model understanding);
2. Offers a readable structure that supports hierarchical organization;
3. Provides compact prompts and token reduction;
4. Facilitates multitasking learning;
5. Avoids ambiguity;
6. Balances flexibility and structure, benefiting complex tasks.
7. Allows models to follow context and multiple examples with greater fidelity.

## 📚 Referências

1. What is prompt engineering?
2. The Prompt Report: A Systematic Survey of Prompt Engineering Techniques
3. ReaderLM‑v2: Small Language Model for HTML to Markdown and JSON
4. Does Prompt Formatting Have Any Impact on LLM Performance?
5. MDEval: Evaluating and Enhancing Markdown Awareness in Large Language Models

#DataScience #GenerativeAI #AgenticAI #AI #ML