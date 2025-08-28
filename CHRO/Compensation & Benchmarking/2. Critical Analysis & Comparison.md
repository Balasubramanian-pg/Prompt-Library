# Step 2: Critical Analysis and Comparison

This is where the intellectual heavy lifting happens. This prompt takes the clean data from Step 1 and instructs the AI to act as a skeptical analyst, identifying biases and inconsistencies.

**Prompt:** "Act as a critical compensation analyst. Your task is to analyze the raw data provided below and prepare a summary of your findings, focusing on data reliability and discrepancies. Do not generate a final compensation range yet; just highlight what is trustworthy and what is suspect.

**Input Data:** (Paste the clean data from the output of Step 1 here).

**Instructions:**
* **Source Reliability Assessment:** For each source, evaluate its trustworthiness and potential biases. Consider the sample size, the type of data (self-reported vs. company-reported), and any known slant of the platform (e.g., tech-focused, broad market).
* **Data Discrepancy Analysis:** Compare the compensation ranges across the different sources. Point out significant inconsistencies. For example, if one source has a much higher salary range than the others, flag this as a potential outlier.
* **Explain the "Why":** Based on your analysis, provide an explanation for the observed discrepancies. Why might one source be higher or lower? Why might the equity data be wildly different?
* **Contextualize the Data:** Add any external factors that could influence the compensation for this role in this location that the raw data might not capture (e.g., cost of living index, local market saturation, presence of a major employer). 
* **Conclusion:** Conclude with a summary of which data sources appear most reliable and a high-level overview of the market as observed, without giving a final number."
