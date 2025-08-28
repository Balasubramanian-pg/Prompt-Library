## Comp Benchmarking

**Task:** Act as a compensation analyst. Your goal is to generate a comprehensive compensation report for a given job title and location by synthesizing data from multiple public sources.

**Input Variables:**
* `JobTitle`: The exact job title (e.g., "Senior Software Engineer").
* `Location`: The city and state/country (e.g., "San Francisco, CA" or "London, UK").
* `ExperienceLevel`: The target experience level (e.g., "Entry-Level," "Mid-Career," "Senior," "Principal").
* `DataSources`: A list of public data sources to be used for the analysis (e.g., "Levels.fyi," "Payscale," "Glassdoor," "Bureau of Labor Statistics").

**Prompt Structure:**

1.  **Objective:** Clearly state the goal: "Generate a detailed compensation report for `{JobTitle}` at the `{ExperienceLevel}` level in `{Location}`."
2.  **Data Retrieval & Synthesis:**
    * Iterate through the `DataSources` list. For each source, retrieve and summarize the publicly available compensation data (base salary, bonus, equity/stock options, total compensation).
    * Note any specific methodologies or disclaimers from each source (e.g., "Payscale data is based on self-reported salaries," "Levels.fyi focuses on tech companies").
3.  **Analysis & Benchmarking:**
    * Compare and contrast the data points across all sources. Identify a central tendency (e.g., median or average) for each compensation component.
    * Establish a compensation range (e.g., 25th to 75th percentile) for base salary and total compensation, noting any outliers.
    * Segment the data by relevant factors such as company size, industry (if available), or type of company (e.g., startup vs. large enterprise).
4.  **Report Generation:**
    * Present the findings in a clear, structured format. The report should include:
        * A summary of the overall compensation range for the role.
        * A breakdown of each compensation component (base, bonus, equity).
        * A section on data source reliability and limitations.
        * An analysis of potential influencing factors (e.g., specific skills, company tier).
    * Conclude with a final, synthesized compensation range that represents the most probable market rate, providing a rationale for the conclusion.

***

### Analysis and Counterpoints

#### Assumptions in the Master Prompt

The prompt is built on several key assumptions that may not hold true, and a good intellectual sparring partner should challenge them.

1.  **Assumption:** Public data is accurate and representative.
    * **Counterpoint:** A significant portion of public compensation data is **self-reported**. This can lead to selection bias, as individuals who are more engaged in career-related forums or who feel they are underpaid/overpaid might be more likely to report their salaries. The data can be noisy and may not accurately represent the broader market, especially for non-tech or niche roles. The data from these sources often lacks verification.

2.  **Assumption:** Aggregating data from different sources is a valid methodology.
    * **Counterpoint:** Each source uses a different methodology for data collection and reporting. Levels.fyi is heavily skewed toward top-tier tech companies. Payscale's data is broader but less granular. Glassdoor's data can be outdated or based on a small sample size for a given role. Simply averaging or synthesizing these disparate datasets without a robust weighting or normalization process could produce a misleading and unreliable result.

3.  **Assumption:** A single compensation range can be applied to a broad job title.
    * **Counterpoint:** The same job title can have dramatically different responsibilities and required skill sets across companies. A "Data Scientist" at a large financial institution may earn and do very different things than a "Data Scientist" at a small e-commerce startup. The prompt's focus on a single, aggregated range overlooks the critical nuance of job responsibilities, specific skills (e.g., Python vs. R, machine learning vs. business intelligence), and the size/type of company. The market is not a single point; it's a dynamic, multi-faceted landscape.

#### Testing the Reasoning

The logic of the prompt is to "synthesize" data to find a "central tendency." This logic is sound, but its application is flawed if it doesn't account for the **quality and context of the data**. The prompt asks to "compare and contrast," but it doesn't explicitly require the model to critically **evaluate the validity** of each source or to provide a confidence interval for the final result.

A more rigorous approach would be to:
* Identify the sample size for each data source for the specific role and location.
* Exclude or de-prioritize sources with very low sample sizes.
* Mention the potential for survivorship or selection bias in self-reported data.
* Instead of a single range, offer a more nuanced view, such as "Tier 1 Tech Companies" vs. "General Market" ranges.

#### Alternative Perspectives

* **A "Tiered" Approach:** Instead of a single master prompt, a better approach might be to create a set of prompts or sub-tasks. The first prompt could be a **data collection and cleaning** task, followed by a second prompt for **critical analysis and comparison**, and a final one for **reporting**. This separates the "gathering" from the "thinking."
* **The "Analyst" Persona:** The prompt sets the persona of a "compensation analyst," but it doesn't give the persona a critical, skeptical voice. A better prompt might instruct the model to "provide a critical analysis, including an assessment of data reliability and potential biases," forcing a more truth-oriented response rather than a simple aggregation.
* **The "Negotiation Partner" Approach:** The goal could be reframed from "generating a report" to "preparing for a salary negotiation." This reframing would require the model to not just provide a range but also to identify the data points that support the high end of the range and the factors that could be used to justify a higher salary. This shifts the focus from a purely descriptive task to a more strategic and actionable one.
