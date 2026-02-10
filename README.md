# Master Mix Calculator

A flexible utility for calculating reagent volumes for laboratory master mixes. While pre-configured for PCR, this calculator can be customized for any multi-component solution.  I used a variety of AI tools to consolidate features from an outdated tool I built years ago and make the UI cleaner.

## 🧪 Features
* **Dynamic Components**: Add or remove reagents and customize component names to suit your protocol.
* **Concentration Agnostic**: Input stock and final concentrations in any units, as long as they remain consistent.
* **Automatic Water Calculation**: Automatically determines the volume of water needed to reach your target master mix volume.
* **Error Detection**: Alerts you if the total component volume exceeds the target master mix volume, suggesting a concentration or fold-change adjustment.

---

## 🚀 How to Use

1. **Define Components**: Enter the **Stock** and **Final** concentration for each reagent.
2. **Set Master Mix Fold (X)**: Specify the concentration factor of your master mix (e.g., 2, 5, or 10).
3. **Set Volume Parameters**:
    * **Reaction Volume ($\mu L$):** The volume of a single reaction.
    * **Number of Reactions:** The total quantity of reactions you plan to prepare.
4. **Review Results**: The program returns the required volume for each stock component and the necessary volume of water.

---

## 📐 Calculations & Logic

The calculator uses the standard dilution formula for each component:

$$V_{stock} = \frac{C_{final} \cdot V_{total}}{C_{stock}}$$

Where:
* $V_{total}$ is calculated based on the Master Mix Fold and the total number of reactions.
* The **Water Volume** is determined by:  
  $V_{water} = V_{MasterMix} - \sum V_{components}$.

---

## 💾 Exporting Data
Click the **Export CSV** button to download your calculation table for use in lab notebooks or record keeping.



<img width="959" height="648" alt="Screenshot 2026-02-10 at 8 10 25 AM" src="https://github.com/user-attachments/assets/90ae9491-6ec5-41ac-98e1-e9934f7342cb" />
