# task-1-prodigy-infotech
n this task, I worked with the Diabetes dataset and created bar charts and histograms to visualize the distribution of categorical and continuous variables such as age and diabetes outcome. This helped me better understand data distribution, trends, and the importance of visualization in simplifying complex data insights.
import pandas as pd
import matplotlib.pyplot as plt

# Load the dataset
df = pd.read_csv('/content/diabetes.csv')

# View first few rows
df.head()
plt.figure()
plt.hist(df['Age'], bins=10)
plt.xlabel('Age')
plt.ylabel('Frequency')
plt.title('Distribution of Age in Diabetes Dataset')
plt.show()

# Count values of Outcome
outcome_counts = df['Outcome'].value_counts()

plt.figure()
plt.bar(outcome_counts.index, outcome_counts.values)
plt.xlabel('Outcome (0 = Non-Diabetic, 1 = Diabetic)')
plt.ylabel('Count')
plt.title('Distribution of Diabetes Outcome')
plt.show()
