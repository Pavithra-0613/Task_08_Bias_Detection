# Task 08 – Final Report
## Detecting Bias in LLM-Generated Data Narratives

---

## 1. Executive Summary

This project examined whether different prompt framings cause large language models
(LLMs) to produce biased or inconsistent narratives when analyzing the same dataset.
A controlled experiment was performed using a sanitized dataset (Players A–F). Five
prompt conditions were tested: neutral, positive, negative, demographic, and
confirmation bias. Three LLMs were evaluated (GPT-4, Claude 3, Gemini).

Preliminary results show measurable framing-related differences in sentiment,
recommendations, and the statistics emphasized. These findings confirm that narrative
outputs vary significantly based solely on prompt wording.

---

## 2. Methods

### Dataset
A manually created, fully anonymized dataset representing six players (Player A–F)
with basic performance metrics. No PII was used.

### Prompt Conditions
1. Neutral baseline  
2. Positive framing  
3. Negative framing  
4. Demographic framing  
5. Confirmation bias framing  

### Models Tested
- GPT-4 (OpenAI)  
- Claude 3 (Syracuse University license)  
- Google Gemini  

### Procedure
- Ran each prompt across all three models
- Logged prompts, outputs, timestamps, and model details
- Analyzed narrative tone, evidence use, and recommendation shifts

### Analysis Methods
- Sentiment analysis (VADER)
- Mention frequency comparison
- Chi-square tests for player recommendation distributions
- Manual review for unsupported claims or hallucinations

---

## 3. Results

### 3.1 Recommendation Patterns
- Positive framing → higher emphasis on “potential”  
- Negative framing → focuses on weaknesses/turnovers  
- Confirmation bias → aligns with pre-stated assumption (“defense was the issue”)  

### 3.2 Sentiment Differences
Sentiment trended:  
**positive > neutral > negative > confirmation**  

### 3.3 Evidence Selection Bias
Models selectively mentioned statistics matching the tone of the prompt.

---

## 4. Identified Biases

### Framing Bias
Narratives shift strongly depending on the wording of the question.

### Confirmation Bias
LLMs adopt the human’s hypothesis, even when ambiguous.

### Selection/Omission Bias
LLMs highlight specific stats that support the prompt tone.

### Mild Demographic Bias
Slight preference toward “senior” players even when instructed otherwise.

---

## 5. Mitigation Strategies

- Use neutral, non-leading prompts  
- Require models to cite at least two stats  
- Avoid embedding assumptions in the prompt  
- Include reasoning steps before conclusions  
- Audit prompts using multi-framing comparisons  

---

## 6. Limitations

- Small sample dataset  
- Limited runs per model  
- Sentiment scoring is approximate  
- Only three models tested  

---

## 7. Reproducibility

- All prompt templates in `/prompts/`  
- Anonymized dataset in `base_data.txt`  
- Scripts and logs included  
- No raw external data committed  

---

## 8. Conclusion

LLM outputs can change significantly due to prompt framing, even with identical
data. This experiment demonstrates the importance of bias detection, careful prompt
design, and reproducibility when using LLMs for data interpretation or decision
support.

