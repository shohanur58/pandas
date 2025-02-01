# pandas
import pandas as pd
data = { 
       "Month":["January","January","February","February","March"],
       "Catagory":["Rent","Groceries","Utilitlies","Entertainment","Transportion"],
       "Amount":[500,200,300,150,100]
}
print(data)
df = pd.DataFrame(data)
print("The Data Frame\n",df)
monthly_expanse = df.groupby("Month")["Amount"].sum()
print("The monthly Expanse\n",monthly_expanse)
highest_month = monthly_expanse.idxmax()
highest_total = monthly_expanse.max()
print(f"The month with the highest total expanse {highest_month} is :{highest_total }")
