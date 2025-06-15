# 🧪 Emoji Payment Funnel A/B Test Analysis

This project simulates and analyzes an A/B test comparing two different emoji monetization strategies in a chat app, using a step-by-step conversion funnel.

## 🔍 Project Overview

The goal is to evaluate whether introducing filtering steps (i.e., pre-qualification) before showing payment prompts affects user conversion rates through the payment funnel.

- **Group A**: Direct payment path (Step 0 → 3 → 4 → 5)
- **Group B**: Filtered path with intermediate steps (Step 0 → 1 → 2 → 3 → 4 → 5)

## 📁 Files Included

- `emoji_ab_test_analysis.ipynb`: Full Colab notebook for data analysis and visualization
- `ab_test_data.csv`: Simulated A/B test dataset
- `funnel_comparison.png`: Bar chart visualization of conversion rates
- `README.md`: Project documentation

## 🧷 Funnel Steps

| Step | Description                  |
|------|------------------------------|
| 0    | Emoji Panel Popup            |
| 1    | Emoji Panel Interacted       |
| 2    | Clicked Specific Emoji       |
| 3    | Payment Guide Shown          |
| 4    | Clicked Payment Button       |
| 5    | Payment Success              |

## 📊 Key Metrics & Results

| Step     | Group A | Group B | p-value | Statistically Significant |
|----------|---------|---------|---------|----------------------------|
| Step 1   | 100%    | 100%    | N/A     | ❌ No                      |
| Step 2   | 100%    | 68.2%   | 0.0000  | ✅ Yes                     |
| Step 3   | 63.8%   | 64.7%   | 0.5110  | ❌ No                      |
| Step 4   | 61.9%   | 23.3%   | 0.0000  | ✅ Yes                     |
| Step 5   | 22.8%   | 20.0%   | 0.0068  | ✅ Yes                     |

> 🔺 Group A achieves higher payment conversions with a simplified funnel.

## 🧠 Insights

- **Group A** has a higher absolute conversion rate in final steps, suggesting less friction leads to better results.
- **Group B** filters out less-engaged users early, but this does not significantly increase quality or final conversions.
- All statistically significant differences were validated using independent **t-tests**.

## 📌 Tools & Stack

- Python (Pandas, SciPy, Matplotlib)
- Google Colab
- GrowthBook (recommended for live experimentation platform)

## 📈 Visual Output

<img  src="https://github.com/user-attachments/assets/86f401e1-633e-4d69-8fe5-fbc0c4110e58"  width="450">

## ✅ Conclusion

A simplified funnel (Group A) leads to significantly higher conversion rates at payment-related stages. Pre-qualification (Group B) adds friction without notable benefits in this simulated context.

