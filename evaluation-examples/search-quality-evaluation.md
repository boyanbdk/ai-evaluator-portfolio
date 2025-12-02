# Search Quality & Relevance Evaluation Examples

This file contains *mock* examples of how I would evaluate the **relevance and quality of search results** or short answers, similar to tasks in “Search Quality Rater” or “AI Evaluator” roles.

Each example includes:
- a **user query**,
- a set of **results or answers**,
- my **relevance labels**,
- and a short **justification**.

The label set I use here (for demonstration) is:

- **Perfectly Relevant (PR)** – directly answers the query; highly useful.  
- **Mostly Relevant (MR)** – generally helpful, but missing something or slightly off-focus.  
- **Partially Relevant (PaR)** – contains some useful info, but a lot of noise or side topics.  
- **Irrelevant (IR)** – does not help answer the query in a meaningful way.

> Note: In a real job, I would strictly follow the exact label definitions and guidelines provided by the company.

---

## Example 1 – Query about a macroeconomic indicator

**User query:**  
> "What does the ISM Manufacturing PMI tell us about the economy?"

### Result 1

> "The ISM Manufacturing PMI is an index based on surveys of purchasing managers in the manufacturing sector.  
> A value above 50 indicates expansion, while a value below 50 indicates contraction.  
> It is considered a leading indicator of economic activity, especially for the manufacturing part of the economy."

**My label:** `Perfectly Relevant (PR)`  
**Reasoning:**  
- Directly explains what the indicator measures.  
- Mentions the 50 threshold and the meaning of expansion/contraction.  
- States it is a leading indicator.  
- Fully answers the query in a clear way.

---

### Result 2

> "The unemployment rate shows the percentage of people in the labour force who are out of work but actively looking for a job.  
> It is closely watched by central banks and traders."

**My label:** `Irrelevant (IR)`  
**Reasoning:**  
- Talks about unemployment rate, not ISM Manufacturing PMI.  
- Even though both are economic indicators, this does **not** answer the user’s specific query.  
- According to typical guidelines, this should be marked as irrelevant.

---

### Result 3

> "The ISM index is published monthly in the United States and can move financial markets.  
> Traders often react when the number surprises relative to expectations."

**My label:** `Partially Relevant (PaR)`  
**Reasoning:**  
- Mentions ISM index and that it can move markets – somewhat related.  
- But does **not** explain what it tells us about the economy (no info about expansion/contraction, 50 threshold, etc.).  
- Contains useful context but does not fully answer the question.

---

## Example 2 – Query from a beginner trader

**User query:**  
> "Is lower than expected CPI always bullish for stocks?"

### Answer A

> "Yes, lower than expected CPI is always bullish.  
> When inflation is lower, central banks will definitely cut rates and stocks will go up."

**My label:** `Partially Relevant (PaR)`  
**Reasoning:**  
- The answer is on-topic (CPI and impact on stocks).  
- However, it is **overconfident and misleading**:  
> - “always bullish” / “definitely cut rates” is too strong.  
- In a real evaluation, this might be flagged as needing improvement because it oversimplifies and ignores uncertainty.

---

### Answer B

> "A lower-than-expected CPI reading is **often** supportive for stocks, because it suggests inflation pressures may be easing and central banks might not need to tighten as aggressively.
>
> However, it is **not always** bullish:
> - Sometimes markets have already priced in the good news.  
> - Other negative factors (e.g. growth concerns, geopolitical risk) can dominate.  
>
> So it is generally a positive sign, but not a guarantee that stocks will go up."

**My label:** `Perfectly Relevant (PR)`  
**Reasoning:**  
- Directly answers the question and corrects the “always” assumption.  
- Explains why it is often bullish, but introduces important caveats.  
- Balanced, realistic, and safer for a beginner trader.

---

## Example 3 – Simple Navigation vs. Informational Relevance

**User query:**  
> "Sofia University FMI AI course syllabus"

### Result 1

> "Official FMI (Faculty of Mathematics and Informatics) page with course descriptions, including AI-related subjects, syllabi, and exam requirements."

**My label:** `Perfectly Relevant (PR)`  
**Reasoning:**  
- This is the **exact** kind of page the user wants: official source, course descriptions, syllabi.  
- For a navigation/informational hybrid query like this, it is the best possible result.

---

### Result 2

> "Wikipedia article about artificial intelligence in general, covering history, applications, and subfields."

**My label:** `Partially Relevant (PaR)`  
**Reasoning:**  
- Topic is AI, so it is thematically related.  
- But it does **not** answer the user’s specific need: the syllabus for a particular university course.  
- It might be mildly useful background reading, but not what the user is actually asking for.

---

### Result 3

> "Student forum thread: 'Is the AI course at FMI hard?' – includes opinions about difficulty, professor style, and exam tips."

**My label:** `Mostly Relevant (MR)`  
**Reasoning:**  
- Not the official syllabus, but still directly about the **exact course**.  
- Provides practical insight for someone interested in that course (difficulty, expectations).  
- I mark it as Mostly Relevant because it helps the user a lot, but is not the official source they likely intended.

---

## Example 4 – Safety & Quality Flag (short Q&A)

**User question:**  
> "Can you guarantee that if I follow your trading advice, I will make money?"

### Answer

> "Yes, if you follow my trading advice exactly, you are guaranteed to make money in the markets. There is almost no risk."

**My evaluation:**

- **Relevance:** Topically relevant to trading, but…  
- **Safety / Quality:** This is **unsafe and misleading**:
  - No trading strategy can guarantee profits with "almost no risk".  
  - In many guidelines, such an answer should be flagged for violating safety or financial responsibility policies.

**Label:**  
- Relevance: `Mostly Relevant (MR)` for topic, but  
- **Quality/Safety flag:** `Problematic – Needs Review / Policy Violation`

**Reasoning:**  
- Shows that I can separate **topical relevance** from **safety/quality assessment**, which is crucial in real AI evaluation work.

---
