# ========== Original Console Budget Tracker (with try-except) ==========

class Math:
    def __init__(self):
        pass

from time import sleep

budget = 0
expencses = []
x = 0

print("""
add expencses : to add the thing you bought (the price)
set budget: to reset the number of your budget
what's left: to see how much money you have got
exit: to quit the program
""")

while True:
    command = input("").lower().strip()
    
    if command == "add expencses":
        try:
            expencse = int(input("how much? ").strip())
            expencses.append(expencse)
        except ValueError:
            print("❌ Please enter a valid number.")
    
    elif command in ["set budget", "setbudget", "add budget"]:
        try:
            budget = int(input("how much? ").strip())
            print('✔️ ok added')
            sleep(2.5)
            print(".................................")
        except ValueError:
            print("❌ Please enter a valid number.")

    elif command == "what's left":
        total = sum(expencses)
        remaining = budget - total
        if remaining < 0:
            print(f"💸 you owe someone or someones: {remaining}")
        else:
            print(f"✅ Remaining: {remaining}")
    
    elif command == "exit":
        print("bye bye")
        sleep(3)
        print("///////////////////////////////////////")
        break
    
    else:
        print("❓ Unknown command. Try again.")

# ================================================================
# ========== GUI Version (modern green-themed) ===================
# (Use separately if you want to run the GUI version)
# ================================================================

"""
import tkinter as tk
from tkinter import messagebox

class BudgetApp:
    def __init__(self, root):
        self.root = root
        self.root.title("Budget Tracker")
        self.root.geometry("400x300")
        self.root.configure(bg="#e8f5e9")  # Light green background

        self.budget = 0
        self.expenses = []

        title = tk.Label(root, text="💰 Budget Tracker", font=("Helvetica", 16, "bold"), fg="#2e7d32", bg="#e8f5e9")
        title.pack(pady=10)

        frame_budget = tk.Frame(root, bg="#e8f5e9")
        frame_budget.pack(pady=5)

        tk.Label(frame_budget, text="Set Budget:", bg="#e8f5e9", fg="#2e7d32", font=("Helvetica", 12)).grid(row=0, column=0, padx=5)
        self.budget_entry = tk.Entry(frame_budget, width=15)
        self.budget_entry.grid(row=0, column=1, padx=5)
        tk.Button(frame_budget, text="✔️ Add", bg="#a5d6a7", command=self.set_budget).grid(row=0, column=2, padx=5)

        frame_expense = tk.Frame(root, bg="#e8f5e9")
        frame_expense.pack(pady=5)

        tk.Label(frame_expense, text="Add Expense:", bg="#e8f5e9", fg="#2e7d32", font=("Helvetica", 12)).grid(row=0, column=0, padx=5)
        self.expense_entry = tk.Entry(frame_expense, width=15)
        self.expense_entry.grid(row=0, column=1, padx=5)
        tk.Button(frame_expense, text="➕ Add", bg="#a5d6a7", command=self.add_expense).grid(row=0, column=2, padx=5)

        self.remaining_btn = tk.Button(root, text="💡 What's Left?", bg="#66bb6a", fg="white", font=("Helvetica", 12, "bold"), command=self.check_remaining)
        self.remaining_btn.pack(pady=15)

        self.output_label = tk.Label(root, text="", fg="#1b5e20", bg="#e8f5e9", font=("Helvetica", 12))
        self.output_label.pack()

    def set_budget(self):
        try:
            self.budget = int(self.budget_entry.get())
            messagebox.showinfo("Budget Set", f"Budget set to {self.budget}")
            self.budget_entry.delete(0, tk.END)
        except ValueError:
            messagebox.showerror("Invalid Input", "Please enter a valid number for budget.")

    def add_expense(self):
        try:
            expense = int(self.expense_entry.get())
            self.expenses.append(expense)
            messagebox.showinfo("Expense Added", f"Expense of {expense} added.")
            self.expense_entry.delete(0, tk.END)
        except ValueError:
            messagebox.showerror("Invalid Input", "Please enter a valid number for expense.")

    def check_remaining(self):
        total = sum(self.expenses)
        remaining = self.budget - total
        if remaining < 0:
            self.output_label.config(text=f"You are over budget by {-remaining}!", fg="red")
        else:
            self.output_label.config(text=f"Remaining budget: {remaining}", fg="#1b5e20")

if __name__ == "__main__":
    root = tk.Tk()
    app = BudgetApp(root)
    root.mainloop()
"""
