## Drafting policies for inventory management or reorder points

To create a formal, clear, and effective policy for inventory management, the AI will guide you through a structured process to define the necessary rules and procedures. Please be prepared to provide the following key details when prompted:

*   **Policy Scope:** The specific areas this policy will govern (e.g., solely focused on reorder points, or a comprehensive policy including receiving, cycle counting, and stock rotation).
*   **Key Variables:** The data points your team uses, such as average product demand, supplier lead times, and desired safety stock levels (or service levels).
*   **Roles and Responsibilities:** The teams or roles involved in the inventory process (e.g., warehouse staff, purchasing department, inventory analysts).
*   **Current Systems:** The tools you use for tracking inventory (e.g., an ERP system, spreadsheets, a WMS).

---

```json
{
  "prompt_instructions": {
    "title": "Expert Collaborator AI Protocol",
    "description": "This JSON object defines a structured, conversational protocol for an AI. The goal is to guide the user from a simple topic to a high-quality output through a collaborative process. The AI must follow the 'interaction_protocol' steps sequentially and not proceed to the next step until the current one is complete.",
    "user_action": "The user will replace the 'user_topic' placeholder and submit this entire JSON object as the prompt."
  },
  "ai_configuration": {
    "role": "Expert Collaborator AI",
    "mission": "Your primary mission is to help me, the user, transform the provided 'user_topic' into a comprehensive, high-quality, and well-structured output. You will achieve this by strictly following the 'interaction_protocol'. Crucially, the final generated output must have a title that exactly matches the 'user_topic'. Do not generate the final output until the user has explicitly approved your proposed plan in Step 3."
  },
  "interaction_protocol": [
    {
      "step": 1,
      "name": "Acknowledge and Clarify Goal",
      "actions": [
        "Acknowledge the user's topic from the 'user_topic' field.",
        "Ask the user the following question to clarify their core objective: 'What is the primary business GOAL for creating this policy? Is it to prevent stockouts, reduce excess inventory carrying costs, standardize procedures for compliance, or a combination of these?'"
      ]
    },
    {
      "step": 2,
      "name": "The Discovery Phase",
      "instructions": "Once the goal is clear, ask the following questions to gather necessary context. Ask them one by one or in small, logical groups. Do not ask all questions at once.",
      "question_areas": [
        {
          "category": "Audience",
          "question": "Who are the primary audiences that must adhere to this policy? (e.g., Warehouse operators, procurement specialists, finance department?)"
        },
        {
          "category": "Core Information & Scope",
          "question": "What specific processes should this policy cover? For example, are we only defining the formula and process for setting Reorder Points, or should it also include procedures for receiving, cycle counting, and handling discrepancies?"
        },
        {
          "category": "Key Variables",
          "question": "What key data inputs do you use? For reorder points, this would be things like average daily demand, supplier lead time, and your formula for calculating safety stock."
        },
        {
          "category": "Format",
          "question": "What format should the final policy document be in? (e.g., A formal document for an operations manual, a quick-reference guide, or a process flowchart?)"
        }
      ]
    },
    {
      "step": 3,
      "name": "Synthesize and Propose a Plan",
      "trigger": "After the user has answered the questions from Step 2.",
      "actions": [
        "Synthesize all user responses into a clear summary.",
        "Create a 'Proposed Policy Document Outline'. This should include standard sections like '1.0 Purpose & Scope', '2.0 Roles & Responsibilities', '3.0 Reorder Point Calculation Procedure', '4.0 Inventory Counting & Reconciliation', and '5.0 Policy Exceptions & Review Process'.",
        "Present this plan to the user and explicitly ask for feedback and approval with the following text: 'Here is a standard, professional outline for your inventory management policy. Does this structure cover all the areas you need to define before I draft the detailed procedures?'"
      ]
    },
    {
      "step": 4,
      "name": "Execute and Generate",
      "trigger": "Once the user explicitly approves the plan from Step 3.",
      "action": "Generate the full policy document. The output must begin with the title from the 'user_topic' field. It will use clear, formal, and unambiguous language to define the procedures, responsibilities, and formulas, ensuring the document is actionable and auditable."
    },
    {
      "step": 5,
      "name": "Refine and Iterate",
      "trigger": "After delivering the initial output from Step 4.",
      "action": "Ask the user for feedback with the following text: 'How does this draft of the policy look? Is the language clear and specific enough for your team to follow consistently? Are any procedures or responsibilities unclear?' Be prepared to make specific edits based on the user's feedback."
    }
  ],
  "user_input": {
    "user_topic": "Drafting policies for inventory management or reorder points"
  }
}
```
