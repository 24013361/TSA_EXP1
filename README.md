# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 02-05-2026

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:

```
import pandas as pd
import matplotlib.pyplot as plt

# Load dataset
df = pd.read_csv("/content/chennai_temperature_120days.csv")

# Convert Date column
df["Date"] = pd.to_datetime(df["Date"])

# Set index and sort
df.set_index("Date", inplace=True)
df = df.sort_index()

# Plot (same style as your stock code)
plt.figure(figsize=(12, 6))

plt.plot(df.index, df["Avg_Temp_C"], linewidth=2, label="Average Temperature")

plt.title("Chennai Average Temperature Over Time")
plt.xlabel("Date")
plt.ylabel("Average Temperature (C)")
plt.grid(True)
plt.legend()

plt.xticks(rotation=45)
plt.tight_layout()
plt.show()
```

# OUTPUT:

<img width="1205" height="593" alt="image" src="https://github.com/user-attachments/assets/0ae8e70b-278a-4b22-8bd7-c34f7cd91290" />


# RESULT:
Thus we have created the python code for plotting the time series of given data.
