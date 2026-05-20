# Fuzzy Expert System for Car Purchase Evaluation

## Overview
This project implements a Fuzzy Logic Expert System designed to help buyers make objective, data-driven decisions when purchasing a second-hand vehicle. 

## The Problem
Buying a car involves weighing multiple, often conflicting factors. A vehicle might have a highly attractive price but suffer from terrible fuel efficiency, or offer premium comfort but come with exorbitant maintenance costs. Standard binary filters fail to capture these real-world trade-offs, making it difficult for average consumers to identify true value versus hidden financial traps.

## The Solution
This system translates expert automotive reasoning into a rigorous mathematical model using Fuzzy Logic. It evaluates **8 key parameters** (Budget Deviation, Maintenance Costs, Fuel Efficiency, Mileage, Ownership History, Comfort, Condition, and Safety) against a custom knowledge base of **21 IF-THEN rules**. The system calculates a precise suitability score and provides a clear recommendation, helping buyers confidently identify the best options while automatically vetoing unsafe or highly risky deals.

## Project Structure
* `main.ipynb` - The core logic engine, including fuzzy variables, the rule base, and custom visualization outputs.
* `A Fuzzy Expert System for the Selection of the Right Car Model` - The comprehensive project report, detailing the methodology and real-world validation cases.
* `README.md` - Project documentation.
* `.gitignore` - Git configuration file.