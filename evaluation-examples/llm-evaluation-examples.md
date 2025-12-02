# LLM Evaluation Examples (A vs B)

In this file, I create **mock examples** of AI answers (A and B) and show how I would evaluate them as an AI evaluator.

Each example includes:
- Task description,
- Answer A,
- Answer B,
- My evaluation (which is better and why),
- Criteria used (accuracy, completeness, clarity, style, safety, etc.).

These are manually written examples to illustrate my reasoning.

---

## Example 1 – Summarising Macroeconomic News for a Trader

**Task:**  
Summarise the impact of the following macro data on risk assets (stocks, crypto) for a short-term trader:
- US CPI came in slightly below consensus.
- Unemployment is stable.
- Fed communication remains cautious but hints at possible cuts next year.

---

### Answer A

> The news is very bullish. CPI is lower so inflation is over, unemployment is fine, and the Fed will cut rates soon.  
> This means stocks and crypto will definitely go up strongly now. It’s a clear buy signal.

### Answer B

> The data is **moderately bullish** for risk assets:
> - **CPI slightly below consensus** suggests that inflation pressures are cooling, which is supportive for risk assets.  
> - **Stable unemployment** indicates the labour market is still healthy, reducing immediate recession fears.  
> - The **Fed’s cautious tone** with hints of possible cuts next year supports the idea that rates may have peaked, but timing is uncertain.
>
> Overall, this creates a mildly positive backdrop for stocks and crypto, but the move is unlikely to be “one-way”.  
> Traders should still watch for:
> - future inflation prints,  
> - changes in labour market data,  
> - any shift in Fed language.

---

### My Evaluation

- **Accuracy:**  
  - A: Overstates the impact; claims inflation is “over” and that prices will “definitely” go up – unrealistic.  
  - B: More realistic and nuanced; acknowledges that data is supportive but not a guarantee.
- **Completeness:**  
  - A: Very short, no mention of risks or uncertainties.  
  - B: Covers CPI, unemployment, Fed tone, and acknowledges uncertainty and monitoring future data.
- **Clarity & Structure:**  
  - A: Simple but shallow.  
  - B: Well-structured with bullet points and clear reasoning.
- **Risk & Safety:**  
  - A: Could mislead traders into thinking it’s a guaranteed “buy”.  
  - B: Clearly avoids deterministic language and highlights risks.

**Conclusion:**  
> **Answer B is clearly better**. It is more accurate, more complete, and safer for a trader, while still providing a bullish interpretation.

---

## Example 2 – Explaining a Basic AI Concept (Heuristic in A* Search)

**Task:**  
Explain what a heuristic is in the context of A* search, to a student who has basic CS knowledge.

### Answer A

> A heuristic is just a guess. In A* you guess how far you are from the goal and add it to the path cost. If the guess is good, the algorithm works.

### Answer B

> In A* search, a **heuristic function** `h(n)` is an estimate of the remaining cost from a node `n` to the goal.
>
> Key points:
> - It is **not exact**, it’s an educated guess.  
> - A* uses `f(n) = g(n) + h(n)`, where `g(n)` is the cost so far, and `h(n)` is the estimated cost to go.  
> - If the heuristic is **admissible** (never overestimates the true cost), A* is guaranteed to find an optimal solution.  
> - A **better (more informed) heuristic** usually means fewer nodes expanded and faster search.
>
> So, a heuristic in A* is a way to guide the search more intelligently than blind methods like uniform-cost or breadth-first search.

---

### My Evaluation

- **Accuracy:**  
  - A: Technically not wrong, but very vague; doesn’t mention admissibility, the role in f(n), or the impact on optimality.  
  - B: Provides correct definition and key properties, including admissibility and impact on performance.
- **Completeness:**  
  - A: Only one vague sentence; missing critical info.  
  - B: Covers definition, formula, optimality condition, and intuitive impact.
- **Clarity:**  
  - A: Too short to be really helpful.  
  - B: Clear, structured, suitable for a CS student.
- **Pedagogical value:**  
  - A: Student may still be confused.  
  - B: Student gets both the concept and why it matters.

**Conclusion:**  
> **Answer B is better** because it is more precise, more informative, and more helpful for learning.

---

## Example 3 – Classifying Sentiment with Justification

**Task:**  
Given a user review, the AI must classify sentiment (Positive / Neutral / Negative) and explain its choice.

**Review:**  
> “The product works okay, but shipping was slow and support didn’t reply to my emails.”

### Answer A

> Sentiment: Positive  
> Explanation: The user says the product works, so they are happy overall.

### Answer B

> Sentiment: Negative  
> Explanation:  
> Although the product “works okay”, the user complains about **slow shipping** and **no reply from support**, which are strong negative signals.  
> Overall, the tone is more frustrated than satisfied, so Negative is the best label.

---

### My Evaluation

- **Accuracy:**  
  - A: Wrong sentiment label; ignores the main negative complaints.  
  - B: Correctly focuses on the most important parts of the review.
- **Justification quality:**  
  - A: Very superficial; ignores the negative content.  
  - B: Explicitly cites the negative phrases and explains the reasoning.
- **Alignment with typical guidelines:**  
  - A: Would likely be flagged as incorrect in an annotation task.  
  - B: Matches common annotation rules: strong negative elements usually dominate.

**Conclusion:**  
> **Answer B is better** because it captures the overall negative tone and explains the decision based on the text.
