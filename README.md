# gitllm

`gitllm` is a public draft of response instructions for language models. It addresses unsupported claims, invented product procedures, unexplained recommendations, excessive agreement, and awkward prose. Its effectiveness has not yet been measured across models.

## Use

Give the model the complete contents of [`gitllm.txt`](gitllm.txt) before your question. If the model can open URLs, you can instead ask it to read the raw file and confirm what it read. A repository name or URL alone does not ensure the model has received the instructions.

The file is self-contained. It is written in English and asks the model to answer in the language the user requests. The Korean example helps illustrate one prose problem; the choice of English has not been shown to improve performance.

## What the instructions try to change

The document asks the model to distinguish supported claims from inference, verify environment-specific steps when possible, state the criterion behind a recommendation, check the user's premise rather than automatically agree, and revise prose that adds performance or repetition. Examples show the intended response to three kinds of question.

This design draws on documented problems and prompt guidance, rather than an established result for this file. OpenAI reported rolling back an April 2025 GPT-4o update after it produced overly agreeable responses. Google's Gemini prompt guide recommends concrete, varied examples for guiding phrasing and response patterns. Neither source demonstrates that `gitllm.txt` works across models.

## Testing

[`tests/cases.md`](tests/cases.md) contains questions and scoring criteria. Run the same questions with and without `gitllm.txt` in separate fresh conversations, using the same model and tool access. Save complete responses, model/version, date, and whether browsing was available. Repeat each condition because responses vary. Publish results, including cases where the instructions make an answer worse. The test cases are proposed tests, not observed outcomes.

## Sources informing the draft

- OpenAI, [Sycophancy in GPT-4o: What happened and what we're doing about it](https://openai.com/index/sycophancy-in-gpt-4o/), April 29, 2025.
- Google AI for Developers, [Prompt design strategies](https://ai.google.dev/gemini-api/docs/prompting-strategies), section on zero-shot and few-shot prompts, accessed September 2026.
- Anthropic, [Demystifying evals for AI agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents), January 9, 2026, on tasks, repeated trials, and grading.

This repository is a working draft. Versioned results should be added before describing the instructions as effective.
