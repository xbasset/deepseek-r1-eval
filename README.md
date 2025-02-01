# DeepSeek-R1-8B Model Evaluation Study

A focused evaluation of DeepSeek-R1-Distill-Llama-8B on a simple counting task: "How many R's are in 'strawberry'?"

## Details of the evaluation

Everything is in the notebook [eval_r1_8b.ipynb](eval_r1_8b.ipynb)

## Results

- 103 total responses analyzed
- 85 correct answers (3 R's)
- 16 incorrect answers (2 R's)
- 2 malformed outputs
- Correct responses had lower token counts (342.0) vs incorrect (386.2)

## Key Findings

The model demonstrates:
- 82.5% accuracy
- Tendency to overthink (longer responses correlate with errors)
- Consistent output format compliance (98%)

## Production Recommendations

1. Run multiple inferences per query
2. Use majority voting
3. Monitor token counts as confidence proxy
4. Implement format validation
5. Have fallback strategies

## Model Details

- Model: [DeepSeek-R1-Distill-Llama-8B](https://huggingface.co/deepseek-ai/DeepSeek-R1-Distill-Llama-8B)
- Task: Simple letter counting
- Format: `<result>X</result>` 