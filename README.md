# Neural Network NBA Draft Combine Predictions: Model Development and Evaluation

**By: Brya Patterson and Nate Lapin** *University of Washington, MS Information Management (MSIM)* *Summer 2025*

## 1. Executive Summary
This project investigates whether NBA Draft Combine performance metrics can accurately predict draft outcomes. Utilizing a longitudinal dataset spanning 2000–2025, we applied exploratory data analysis (EDA) and neural network modeling to evaluate the predictive weight of "pure athleticism" versus historical selection trends. 

Our findings suggest that while physical metrics provide a baseline, the modern NBA draft process increasingly prioritizes multi-dimensional skills and context not captured by combine drills alone.

## 2. Methodology & Data Preparation

### Data Pipeline
* **Source:** A comprehensive dataset of every combine participant from 2000 to 2025.
* **Feature Engineering:** Metrics include:
    * **Anthropometric Data:** Height, Weight, Wingspan.
    * **Performance Data:** Vertical, Agility, Sprint, and Bench Press.
* **Preprocessing:** Standardized measurements for cross-era comparability and handled the 2019 discontinuation of the bench press.

### Model Architecture
We implemented a **Sequential Neural Network** via TensorFlow/Keras:
* **Layers:** Input layer matched to feature dimensions, followed by dense hidden layers with **ReLU activation**.
* **Optimization:** Utilized the **Adam optimizer** and Binary Crossentropy loss to classify prospects as "Drafted" vs. "Undrafted."

## 3. Key Results & Analysis

### Statistical Correlations
* **Athletic Synergy:** A strong positive correlation (0.85) was found between Standing Vertical and Max Vertical jumps.
* **Independent Metrics:** The Bench Press showed very weak correlations with all other athletic metrics, suggesting upper body strength is independent of agility and speed.

### Positional Trends
* **Draft Probability:** Small Forwards (SF) currently hold the highest draft rate (~60%), while Centers (C) face the highest standards for entry (~45% draft rate).
* **Physical Profiles:** Identified specific "sweet spots" for draftability, such as players in the 6'5"-6'8" range weighing between 270-290 lbs.

### Model Performance
* The model achieved a **Recall of 0.80** for the 2025 draft (correctly identifying 36 of 45 drafted players).
* However, high false-positive rates indicate that combine metrics alone provide a "weak signal" for definitive draft decisions.

## 4. Conclusion & Future Work
The research concludes that NBA Draft Combine metrics are insufficient for reliable draft prediction when used in isolation. Modern teams appear to weigh professional production and skill sets more heavily than raw athletic testing.

**Future Iterations will include:**
* Incorporating college and international performance statistics.
* Adding advanced impact metrics (BPM, Win Shares).
* Integrating qualitative scouting report data.

## 5. References
* Hogan, S. R., et al. (2023). *The Athletic Intelligence Quotient and performance in the National Basketball Association.*
* Lapin, N. (2025). *NBA Draft Combine & Player Info + "Drafted?" Data [Data set].*
* Tong, T.-h., & Wang, G.-w. (2024). *Anthropometric and physical fitness indicators in the NBA.*