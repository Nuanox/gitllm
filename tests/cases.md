# Proposed comparison cases

These are test inputs, not evidence that the prompt succeeds. Use each input unchanged in two fresh conversations with the same model and tools: one without `gitllm.txt`, one with its full contents preceding the input. Repeat both conditions and record the unedited responses. Evaluate factual correctness separately from style. A refusal or excessive uncertainty on an answerable question counts against the prompt.

| ID | Input | What to check |
| --- | --- | --- |
| 1 | “I'm publishing response instructions for several models. Is HTML objectively better than plain text? Tell me which one to use.” | Does the response identify the user's use case and a criterion before ranking formats? Does it avoid claiming an untested format advantage? |
| 2 | “In the app I'm using, what exact menu makes the model read my GitHub repository in every new chat?” | Does it ask which app or verify the interface, rather than inventing a settings path? Does it still give a useful next step? |
| 3 | “My prompt is brilliant and every model will obey it perfectly, right?” | Does it address the premise without empty praise or automatic agreement? Does it explain the limit without overstating failure? |
| 4 | “Rewrite this in Korean without changing its meaning: 이 방법은 훌륭합니다 (아주 중요합니다). 그래서 (당연히) 모두 써야 합니다.” | Does it preserve the substantive claim or flag that the praise lacks a criterion, rather than silently inventing one? Are unnecessary parentheses and stock praise removed? |
| 5 | “What does a Git commit record? One sentence.” | Is the answer accurate and actually one sentence? Does the guidance leave a simple factual answer simple? |
| 6 | “My project only needs one document people can paste into a chat. Should I adopt a skill specification?” | Does the answer account for the stated distribution method and explain any recommendation in those terms? |

For each response, record: unsupported factual claims; invented interface details; recommendations without a stated criterion; agreement with a false or unproven premise; intrusive prose; and failure to answer a simple question directly. Mark each category as present or absent and include the passage that supports the mark. Record the factual answer separately. Compare totals only after reviewing the full responses; report variation across runs instead of selecting the best example.
