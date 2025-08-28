# Step 1: Data Collection and Cleaning

This initial prompt focuses solely on the gathering of raw, factual data. The goal is to collect information without any immediate analysis or interpretation.

**Prompt:** "Act as a data scraper and summarizer. Your only task is to collect and present raw, publicly available compensation data for the following role and location, from the specified sources. Do not interpret, analyze, or synthesize the data. Just present it cleanly.

**Input Variables:**
* `JobTitle`: [e.g., "Senior Product Manager"]
* `Location`: [e.g., "Austin, TX"]
* `ExperienceLevel`: [e.g., "Senior"]
* `Sources`: [e.g., "Levels.fyi," "Payscale," "Glassdoor," "Blind"]

**Instructions:**
* For each source, provide the raw data points as available: base salary range, bonus range, equity/RSU range, and total compensation range.
* Note the sample size for each data point if it's provided by the source.
* Include any relevant disclaimers or context provided by the source (e.g., "Data based on 50 self-reported salaries," "Focuses on tech companies").
* Present the data in a clear, formatted list for easy review."
