# 📊 Population Distribution Visualization

A basic data visualization project that uses a bar chart to display population distribution across age groups in India.  
Inspired by the official population pyramid for India (2022), based on UN estimates.

## 🧰 Tools Used

- Python
- Pandas
- Matplotlib
- Seaborn (optional)

## 📂 Dataset

A simplified dataset containing 3 main age groups:

| Age Group     | Population (Millions) | Percentage |
|---------------|------------------------|------------|
| 0–20 Years    | 512                    | 36.1%      |
| 21–64 Years   | 807                    | 57.0%      |
| 65+ Years     | 98                     | 6.9%       |

> You can manually input the data or load it from a CSV file if needed.

## 🚀 Run the Code

```bash
python population_chart.py
📸 Sample Output
(Add a screenshot of the chart output here if you'd like)

📜 License
This project is open-source and free to use under the MIT License.

python
Copy
Edit
---

## 🐍 `population_chart.py` (Main Code)

```python
import matplotlib.pyplot as plt

# Data
age_groups = ['0–20 Years', '21–64 Years', '65+ Years']
population = [512, 807, 98]
colors = ['gold', 'deepskyblue', 'hotpink']

# Plot
plt.figure(figsize=(8, 6))
bars = plt.bar(age_groups, population, color=colors)
plt.title("India's Population Distribution by Age (2022)")
plt.ylabel("Population (in Millions)")
plt.xlabel("Age Groups")

# Add data labels
for bar in bars:
    height = bar.get_height()
    plt.text(bar.get_x() + bar.get_width()/2., height + 5,
             f'{height}M', ha='center', fontsize=11)

plt.tight_layout()
plt.show()
