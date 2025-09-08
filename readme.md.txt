Objective of the Task:

The main objective of this task was to automatically classify and tag customer support tickets into relevant categories using a Large Language Model (LLM).
This reduces the manual effort of support teams, speeds up ticket triaging, and ensures that customer issues are directed to the right department efficiently.


Methodology / Approach:

Dataset:
Free-text support ticket examples were used (e.g., billing issues, technical problems, account access).

LLM Technique Used:
Applied Zero-Shot Learning using Hugging Face’s facebook/bart-large-mnli model.

Zero-shot means the model was not trained on ticket data beforehand but could still classify text into categories using natural language understanding.

Process:
Defined possible ticket categories (e.g., "Billing Issue", "Technical Problem", "Account Access", "Feature Request", "Other").

Passed each ticket to the model with these candidate labels.

Model returned probability scores for each label.

The top 3 most likely tags were selected for each ticket.


Key Results or Observations:

The LLM was able to understand ticket descriptions and classify them into appropriate categories with good accuracy.

For example:

"I was charged twice for my subscription" → correctly tagged as Billing Issue.

"The app keeps crashing when I upload a file" → correctly tagged as Technical Problem.

However, as a general-purpose model, it may sometimes confuse overlapping categories (e.g., "Account locked" could be misclassified between Account Access and Technical Problem).

The zero-shot approach worked well without training, making it quick to implement.

For real-world applications, few-shot learning or fine-tuning on company-specific tickets could further improve accuracy.


Conclusion

This task demonstrated how an LLM can be leveraged for text classification in customer support.
By auto-tagging tickets, businesses can save time, reduce human error, and prioritize urgent issues faster.
It shows the practical potential of LLMs in automating repetitive tasks in customer service.