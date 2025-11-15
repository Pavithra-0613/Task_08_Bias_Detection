# Task 08 – Bias Detection in LLM-Generated Data Narratives

This project investigates whether different prompt framings produce different
narratives, recommendations, and sentiment patterns in large language models.

The experiment uses a sanitized small dataset (Players A–F) and tests 5 prompt
conditions:

1. Neutral baseline
2. Positive framing
3. Negative framing
4. Demographic framing (non-identifying class year)
5. Confirmation bias framing

Models tested:
- GPT-4
- Claude 3 (via Syracuse enterprise license)
- Google Gemini

Results, analysis scripts, and logs are stored in the repo. No datasets or PII
are included. All player names are anonymized as “Player A–F”.

See `REPORT.md` for the final write-up.
