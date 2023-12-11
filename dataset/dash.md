pip install pandas matplotlib seaborn
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load the dataset
file_path = 'dataset/Traffic.csv'
df = pd.read_csv(file_path)

# Plot Histogram
plt.figure(figsize=(10, 6))
sns.histplot(data=df, x='column_name', bins=20, kde=True)  # Replace 'column_name' with the actual column name you want to plot
plt.title('Histogram')
plt.xlabel('X-axis Label')
plt.ylabel('Frequency')
plt.show()

# Plot Heatmap
correlation_matrix = df.corr()  # Calculate correlation matrix
plt.figure(figsize=(12, 8))
sns.heatmap(correlation_matrix, annot=True, cmap='coolwarm', linewidths=.5)
plt.title('Heat Map')
plt.show()
