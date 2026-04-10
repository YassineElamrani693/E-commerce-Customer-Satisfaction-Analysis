# E‑Commerce Customer Satisfaction Analysis

## Overview
This project analyzes customer satisfaction using an e‑commerce dataset of **450 customers**. The goal is to identify key drivers of satisfaction and provide actionable business recommendations. The analysis focuses on overall satisfaction, differences by gender, by membership type (Gold/Silver/Bronze), and the combined effect of membership and gender.

## Dataset
- **File**: `E-commerce Customer Behavior - Sheet1.csv`
- **Rows**: 450 customers (after cleaning)
- **Key columns**: Customer ID, Gender, Age, City, Membership Type, Total Spend, Items Purchased, Average Rating, Discount Applied, Days Since Last Purchase, Satisfaction Level.

## Visualizations & Findings

### 1. Overall Customer Satisfaction
![Overall Satisfaction](OverallCustomerSatisfaction.png)

- **Satisfied**: 36%  
- **Not Satisfied**: 64%  

**Interpretation**: Twice as many customers are unsatisfied as satisfied. There is a broad issue with the overall experience or value proposition.

### 2. Satisfaction by Gender
![Satisfaction by Gender](SatisfactionByGender.png)

| Gender | Satisfied | Not Satisfied | Satisfaction Rate |
|--------|-----------|---------------|-------------------|
| Female | 57        | 115           | 33%               |
| Male   | 67        | 107           | 39%               |

**Interpretation**: Both genders are more likely to be unsatisfied. Men have a slightly higher satisfaction rate (39% vs 33%), but the gap is small. Interventions should not be gender‑targeted.

### 3. Satisfaction by Membership Type
![Satisfaction by Membership Type](SatisfactionByMembershipType.png)

| Membership | Satisfied | Not Satisfied | Satisfaction Rate |
|------------|-----------|---------------|-------------------|
| Gold       | 117       | 3             | 98%               |
| Silver     | 8         | 108           | 7%                |
| Bronze     | 0         | 114           | 0%                |

**Interpretation**: Membership tier is the single biggest driver of satisfaction. Gold members are almost universally satisfied, while Silver and Bronze members are overwhelmingly unsatisfied.

### 4. Satisfaction by Membership Type and Gender (Combined)
![Satisfaction by Membership & Gender](SatisfactionByMembershipTypeAndGender.png)

| Membership | Gender | Satisfied | Not Satisfied | Satisfaction Rate |
|------------|--------|-----------|---------------|-------------------|
| Bronze     | Male   | 0         | 60            | 0%                |
| Bronze     | Female | 0         | 50            | 0%                |
| Gold       | Male   | 58        | 0             | 100%              |
| Gold       | Female | 59        | 5             | 92%               |
| Silver     | Male   | 1         | 18            | 5%                |
| Silver     | Female | 10        | 80            | 11%               |

**Interpretation**: Within each membership tier, men and women show very similar patterns. The small gender differences seen in the overall chart disappear once membership is accounted for. **Membership effects dominate gender effects.**

## Recommendations
1. **Enhance Silver & Bronze value propositions** – Gold members clearly receive compelling benefits. Identify what makes Gold successful and adapt for lower tiers.
2. **Drive upgrades to Gold** – Use targeted promotions, discounts, or added features to convert Silver/Bronze customers.
3. **Fix systemic issues** – Overall dissatisfaction is high (64%). Test improvements on the large unsatisfied segments (Silver & Bronze) for the biggest lift.

## How to Run the Code
1. Clone this repository and ensure the CSV file and all four PNG images are in the same folder.
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn
