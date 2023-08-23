# Empowering-Investors-Hackathon

## README.md must consist of the following information:

#### Team Name - Dynamic Squad
#### Problem Statement - In today's fast-paced world, managing personal finances has become increasingly complex. People often find it challenging to keep track of their expenses, stick to their budgets, and make informed financial decisions. As a result, there is a growing need for a reliable and user-friendly solution that can help individuals effectively manage their personal expenses and budgets.
#### Team Leader Email - keerthanak.ece2022@citchennai.net

## A Brief of the Prototype:
  For the prototype, we as a team actually did a demoo website to how the site will work after developed. This demo gives a clear idea on how the site will be developed in the future.

  ![image](https://github.com/kk150105/Empowering-Investors-Hackathon/assets/143043637/759fb82b-0677-41da-a6cc-4dfe2e41029c)

## Tech Stack: 
   HTML is used for making the prototype.
   
## Step-by-Step Code Execution Instructions:
  class ExpenseCategory:
    def __init__(self, name, budget_limit):
        self.name = name
        self.budget_limit = budget_limit

class PersonalExpense:
    def __init__(self, date, amount, category):
        self.date = date
        self.amount = amount
        self.category = category

class ExpenseManager:
    def __init__(self):
        self.expenses = []
        self.categories = []

    def add_expense(self, expense):
        self.expenses.append(expense)

    def add_category(self, category):
        self.categories.append(category)

  def main():
    manager = ExpenseManager()

    while True:
        print("1. Add Expense")
        print("2. Add Category")
        print("3. View Expenses")
        print("4. View Categories")
        print("5. Exit")
        
        choice = input("Enter your choice: ")

        if choice == '1':
            date = input("Enter date (YYYY-MM-DD): ")
            amount = float(input("Enter amount: "))
            category_name = input("Enter category: ")

            category = None
            for c in manager.categories:
                if c.name == category_name:
                    category = c
                    break

            if category is None:
                print("Category not found.")
                continue

            expense = PersonalExpense(date, amount, category)
            manager.add_expense(expense)
            print("Expense added.")

        elif choice == '2':
            name = input("Enter category name: ")
            budget_limit = float(input("Enter budget limit: "))
            category = ExpenseCategory(name, budget_limit)
            manager.add_category(category)
            print("Category added.")

        elif choice == '3':
            for expense in manager.expenses:
                print(f"Date: {expense.date}, Amount: {expense.amount}, Category: {expense.category.name}")

        elif choice == '4':
            for category in manager.categories:
                print(f"Category: {category.name}, Budget Limit: {category.budget_limit}")

        elif choice == '5':
            print("Exiting.")
            break

        else:
            print("Invalid choice. Please select again.")

if __name__ == "__main__":
    main()

  
## What I Learned:
  This prototypa has showed how website are developed and how it hard to keep track of our own expenses. I also learned how few technologies work.
