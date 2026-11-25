# **Power BI – Invoke Function (Simple Example)**

## **1. What is Invoke Function?**

Invoke Function is used to apply a custom function to each row of a table.

**Example:** Calculate 10% commission on every employee's sales.

## **2. Dataset**

| Employee | Sales |
| -------- | ----- |
| Rohit    | 10000 |
| Priya    | 20000 |
| Amit     | 15000 |
| Neha     | 30000 |
| Rahul    | 25000 |

## **3. Create a Function**

1. Open Power Query Editor.
2. Go to Home → New Source → Blank Query.
3. Rename it `CalculateCommission`.
4. Open Advanced Editor.
5. Write this code:

```
(Sales as number) as number =>
Sales * 10 / 100
```

Click Done.

## **4. Invoke Function**

1. Select the Employee Sales table.
2. Go to Add Column.
3. Click Invoke Custom Function.
4. Enter the following:

| Setting         | Value               |
| --------------- | ------------------- |
| New column name | Commission          |
| Function query  | CalculateCommission |
| Sales           | Sales               |

5\. Click OK.

## **5. Expected Output**

| Employee | Sales | Commission |
| -------- | ----- | ---------- |
| Rohit    | 10000 | 1000       |
| Priya    | 20000 | 2000       |
| Amit     | 15000 | 1500       |
| Neha     | 30000 | 3000       |
| Rahul    | 25000 | 2500       |

## **6. Practice Questions**

1. Create a function to calculate 5% discount.
2. Create a function to calculate 18% GST.
3. Create a function to calculate 15% employee bonus.
4. Create a function to calculate 2% sales commission.

**Remember:**

- Function = Create calculation.
- Invoke Function = Apply calculation to table rows.
