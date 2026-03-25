# analysis.pyimport pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv("real_estate_data.csv")

# Average price by location
avg_price = df.groupby("Location")["Price"].mean()

print("Average Price by Location:")
print(avg_price)

# Bar chart
avg_price.plot(kind='bar')
plt.title("Average Property Price by Location")
plt.xlabel("Location")
plt.ylabel("Price")
plt.show()

# Scatter plot
plt.scatter(df["Size (sqm)"], df["Price"])
plt.xlabel("Size (sqm)")
plt.ylabel("Price")
plt.title("Size vs Price")
plt.show()
