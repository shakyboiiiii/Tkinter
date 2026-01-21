import pandas as pd
import matplotlib.pyplot as plt
df = pd.read_csv("company_sales_data.csv")
plt.figure(figsize=(8,5))
plt.plot(
    df['month_number'],
    df['total_profit'],
    linestyle=':',
    marker='o',
    linewidth=3,
    color='red',
    markerfacecolor='black'
)
plt.xlabel("Month")
plt.ylabel("Profit")
plt.title("Company Profit Per Month")
plt.show()
plt.figure(figsize=(10,6))
plt.plot(df['month_number'], df['facecream'], marker='o', linewidth=3, label='Face Cream')
plt.plot(df['month_number'], df['facewash'], marker='o', linewidth=3, label='Face Wash')
plt.plot(df['month_number'], df['toothpaste'], marker='o', linewidth=3, label='Toothpaste')
plt.plot(df['month_number'], df['bathingsoap'], marker='o', linewidth=3, label='Bathing Soap')
plt.plot(df['month_number'], df['shampoo'], marker='o', linewidth=3, label='Shampoo')
plt.plot(df['month_number'], df['moisturizer'], marker='o', linewidth=3, label='Moisturizer')
plt.xlabel("Month")
plt.ylabel("Sales")
plt.title("Sales Data of All Products Per Month")
plt.legend()
plt.show()
plt.figure(figsize=(10,6))
bar_width = 0.3
plt.bar(
    df['month_number'] - bar_width/2,
    df['facecream'],
    width=bar_width,
    label='Face Cream'
)
plt.bar(
    df['month_number'] + bar_width/2,
    df['facewash'],
    width=bar_width,
    label='Face Wash'
)
plt.xlabel("Month")
plt.ylabel("Sales")
plt.title("Face Cream vs Face Wash Sales Per Month")
plt.legend()
plt.show()
