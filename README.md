Project Sentinel: Multimodal Fraud Intelligence
Bridging the gap between numerical thresholds and contextual risk.
In traditional financial auditing, we often rely on "hard rules"—numerical thresholds like Debt-to-Equity ratios or ROA. However, sophisticated risk doesn't always show up in the balance sheet immediately. It hides in the language of management reports and risk disclosures.

Project Sentinel is a proof-of-concept for a multimodal risk engine. It demonstrates that by fusing structured financial data with unstructured text analysis, we can catch "Shadow Risk" that legacy systems are programmed to ignore.

🧐 The "Threshold Gap"
During this audit, I discovered a significant blind spot in standard rule-based engines:

The Failure: Legacy rules (based on ROA/Debt) flagged 189 fraudulent entities as "Safe" because their financial ratios were within normal ranges.

The Discovery: By applying BART-Large Zero-Shot Classification to the textual disclosures of those same entities, the system identified clear indicators of "Internal Control Weaknesses" and "Compliance Concerns."

The Impact: This simple multimodal check uncovered $47.25M in hidden financial exposure that would have otherwise been approved.

🛠️ How it Works
The project follows a three-stage logic:

Data Fusion: Merging numerical performance metrics with raw textual Risk Disclosures and MD&A (Management's Discussion and Analysis) strings.

Gap Analysis: Simulating a legacy compliance filter to identify "False Negatives"—fraudulent cases that look "numerically healthy."

NLP Intelligence: Using a Zero-Shot learning model to audit the text of those missed cases, assigning a risk label and a confidence score without needing prior training on the specific dataset.

⚖️ Achieving Equilibrium
The goal isn't just to find more fraud—it's to optimize the balance between Detection Integrity and Operational Velocity.

By using high-confidence AI scores, we can:

Reduce Friction: Automatically "Green-light" transactions where both numbers and text indicate safety.

Focus Resources: Direct human investigators only to cases where the AI detects a high-confidence mismatch between reported numbers and textual sentiment.

📂 Project Structure
analysis.ipynb: The full end-to-end walk-through of the audit and AI implementation.

numerical_fraud_dataset.csv / text_fraud_dataset.csv: Simulated data used for the audit.

requirements.txt: Environment dependencies (Transformers, Torch, Plotly, etc.).

🚀 Getting Started
Clone the repo.

Install dependencies: pip install -r requirements.txt.

Run the analysis.ipynb notebook to see the interactive Plotly visualizations and AI audit results.
