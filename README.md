# 🏗️ Construction Bidding Risk Analysis (Monte Carlo Simulation & Sensitivity Analysis)

###  Executive Summary
**The Business Challenge:**
My firm is considering a fixed-bid contract of **$5.5 Million** for a large construction project. However, the underlying costs are volatile. If costs exceed estimates, the project could result in a significant financial loss.

**The Objective:**
Determine the statistical probability of turning a profit and identify the "break-even" risk profile before signing the contract.

**The Solution:**
I built a **Monte Carlo Simulation** model in Python to run **10,000 iterations** of the project lifecycle. By randomizing input variables (Labor, Material, Rehab costs) based on historical volatility, I generated a full risk profile for the project.

---

### Technical Methodology
* **Technique:** Monte Carlo Simulation (10,000 Trials).
* **Tools:** Python (NumPy, Pandas, Matplotlib).
* **Modeling Uncertainty:**
    * *Labor Costs:* Modeled as a Discrete Distribution (Strike-risk weighted).
    * *Material Costs:* Modeled as a Normal Distribution (Market volatility).
    * *Rehab Costs:* Modeled as a Triangular Distribution (Min/Max/Most Likely).

---

### Key Insights & Results

| Metric | Estimated Value |
| :--- | :--- |
| **Average Expected Profit** | **$368,367** |
| **Probability of Loss (< $0)** | **17.2%** |
| **Worst-Case Scenario** | **-$650,000** (approx) |

**Strategic Findings:**
1.  **Risk Exposure:** While the project is profitable on average, there is a **~17% chance** of losing money. This exceeds the company's typical risk tolerance of 15%.
2.  **Sensitivity Analysis:** The model identified that **Labor Cost volatility** is the single biggest driver of variance. A labor strike increases costs by ~$200k, pushing the project into negative territory.
3.  **Recommendation:** Based on the simulation, I recommended **increasing the bid to $5.7M** to buffer against labor risks, or negotiating a "Labor Cost Adjustment" clause.

---

### 📷 Visualization: Profit/Loss Distribution
*The graph below shows the result of 10,000 simulations. The red area represents the risk of loss.*
<img width="998" height="624" alt="download" src="https://github.com/user-attachments/assets/037f6df1-d7c2-47c1-8f70-0fc78c323f7b" />

