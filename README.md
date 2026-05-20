# Fuzzy Logic Expert System for Second-Hand Car Evaluation

A comprehensive Python based decision-support system that utilizes fuzzy logic to evaluate and score second hand vehicle deals. 

When evaluating a used car, human decision-making rarely relies on strict binary conditions. A vehicle isn't instantly rejected for being slightly over budget if it offers exceptional reliability, low mileage, and top tier safety. This project captures those real world compromises—and the inherent "gray areas" of car buying—by implementing a Mamdani fuzzy inference system that mimics the nuanced evaluation process of an automotive expert.

### System Architecture
The engine processes real world market metrics and converts them into fuzzy sets to determine the overall viability of a purchase. The system is built upon **8 explicitly defined input variables (Antecedents):**

1. **Budget Deviation (%):** Measures how much the asking price deviates from the buyer's predefined budget.
2. **Maintenance Costs (0-10):** An estimated score of the vehicle's long-term upkeep and parts expenses.
3. **Fuel Efficiency (km/l):** The car's expected fuel consumption rate.
4. **Mileage (in thousands):** The total distance the car has traveled.
5. **Ownership History (Hand):** The number of previous owners the vehicle has had.
6. **Practicality & Comfort (0-10):** A subjective score representing the car's ergonomics, space, and ride quality.
7. **Car Condition (0-100):** A percentage score reflecting the vehicle's current mechanical and aesthetic state.
8. **Safety Rating (1-5):** The official crash-test safety rating.

**Output Variable (Consequent):**
* **Purchase Suitability (0-1):** A defuzzified score categorizing the deal into one of five linguistic terms: *Definitely Avoid, Poor Choice, Uncertain, Good Choice,* or *Highly Recommended.*

### Fuzzy Logic Implementation
Instead of hard coded thresholds, the engine evaluates inputs through a custom knowledge base of **21 fuzzy IF-THEN rules**, implemented using the `scikit-fuzzy` control module. 

* **Fuzzy Inference:** The crisp input variables are mapped to their respective membership functions (e.g., Poor, Average, Excellent) to determine their degree of truth.
* **Rule Processing:** The control system utilizes fuzzy logic operators (AND / OR) to connect multiple antecedents. This allows the system to process complex multi-variable conditions simultaneously.
* **Defuzzification:** Once all rules are evaluated and their consequent fuzzy sets are truncated, the system aggregates the results. It calculates the center of gravity (Centroid method) of the resulting mathematical area to produce a single, crisp output score. This numerical score is then mapped back to the closest linguistic category to provide the final user verdict.

### Repository Structure
* `main.ipynb`: The primary Jupyter Notebook containing the codebase for defining the fuzzy universes, membership functions, the 21-rule compilation, and the execution of the defuzzification process with custom graphical outputs.
* `A Fuzzy Expert System for the Selection of...`: The full technical project report. It covers the theoretical background, the exact mapping of all rules, and a detailed verification section using authentic market test cases.
* `README.md`: Project documentation and overview.
* `.gitignore`: Standard Git configuration for ignoring local environment files.
