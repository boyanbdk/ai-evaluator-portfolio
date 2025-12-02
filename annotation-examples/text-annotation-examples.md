# Text Annotation Examples

In this file I create small, mock datasets to illustrate how I would approach **text annotation** tasks.

I use simple label sets such as:
- **Sentiment:** Positive / Neutral / Negative  
- **Topic:** Macro / Trading / Personal / Language learning / Other  
- **Relevance to trading decision:** High / Medium / Low

These examples are invented for demonstration purposes.

---

## 1. Sentiment + Topic + Relevance

**Label definitions:**

- **Sentiment**
  - Positive: mainly optimistic / satisfied tone.
  - Neutral: factual, informative, no strong emotion.
  - Negative: complaints, risks, dissatisfaction, strong concern.

- **Topic**
  - Macro: macroeconomic data, central banks, inflation, etc.
  - Trading: specific trades, markets, entries/exits.
  - Personal: everyday life, feelings, schedule.
  - Language: learning or using languages.
  - Other: anything else.

- **Relevance to trading decision**
  - High: directly affects a trading decision or market view.
  - Medium: indirectly relevant to trading context.
  - Low: mostly unrelated to trading.

---

### Example table

| ID | Text snippet                                                                                             | Sentiment | Topic   | Relevance |
|----|----------------------------------------------------------------------------------------------------------|-----------|---------|-----------|
| 1  | "US CPI came in lower than expected, so markets might react positively in the short term."              | Neutral   | Macro   | High      |
| 2  | "I missed today’s move on EUR/USD, but overall my risk management was okay."                             | Mixed/Neutral | Trading | Medium    |
| 3  | "Le soir, je suis trop fatigué pour étudier le français, mais j’essaie au moins 15 minutes."            | Mixed/Neutral | Language | Low       |
| 4  | "The broker’s platform crashed during NFP, which was really frustrating and cost me a good setup."      | Negative  | Trading | High      |
| 5  | "Tomorrow I’ll just chill at home and maybe watch some series, no charts for today."                    | Neutral   | Personal| Low       |

> Note: For real projects, I would follow the **exact** label definitions and edge-case rules specified in the annotation guidelines.

---

## 2. Short Binary Relevance Task (Relevant / Not Relevant)

**Instruction (as in a real task):**  
> Given a short text, label it as **Relevant** if it helps a short-term trader form a view about markets or manage a position. Otherwise, label it **Not relevant**.

| ID | Text snippet                                                                                  | Label      |
|----|-----------------------------------------------------------------------------------------------|-----------|
| 1  | "The Fed chairman will speak in 2 hours about the future path of interest rates."             | Relevant  |
| 2  | "I’m going to the gym after lunch and then meeting friends for coffee."                       | Not relevant |
| 3  | "German manufacturing PMI fell below 50, indicating contraction in the sector."              | Relevant  |
| 4  | "The new season of my favourite series just started on Netflix."                             | Not relevant |
| 5  | "Bitcoin broke above a key resistance level with strong volume during the US session."       | Relevant  |

---

## 3. Simple Quality Flag (Good / Needs Review)

**Instruction:**  
> For each model-generated explanation, label it as **Good** if it is clear, accurate, and aligned with the guidelines, or **Needs review** if it is unclear, incomplete, or potentially misleading.

| ID | Model explanation                                                                                                      | Label         | Short comment                                      |
|----|------------------------------------------------------------------------------------------------------------------------|---------------|----------------------------------------------------|
| 1  | "CPI lower than expected is always bullish and means markets will go up for sure."                                     | Needs review  | Overconfident, "for sure" is misleading.           |
| 2  | "The heuristic in A* search estimates remaining cost to the goal and helps guide the search more efficiently."        | Good          | Short but correct and aligned with guidelines.     |
| 3  | "The review is positive because the user said the product works okay, even though they mention some issues."          | Needs review  | Misinterprets sentiment, ignores main complaints.  |
| 4  | "Stable unemployment reduces immediate recession risks, but future data could change the outlook."                    | Good          | Balanced and cautious wording.                     |

---

These examples are small, but they show:
- that I can define and follow **labeling schemes**,  
- how I think about edge cases and **annotation quality**,  
- and how I might annotate data in a real AI Data Annotation / AI Evaluator role.
