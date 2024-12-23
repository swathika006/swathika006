import tkinter as tk
from tkinter import messagebox

# Function to calculate the weight of each metal in the mixture
def calculate_mixture():
    try:
        # Get the user inputs from the entry fields
        total_weight = float(entry_total_weight.get())
        gold_percentage = float(entry_gold_percentage.get())
        copper_percentage = float(entry_copper_percentage.get())
        aluminum_percentage = float(entry_aluminum_percentage.get())

        # Validate that the total percentage equals 100
        total_percentage = gold_percentage + copper_percentage + aluminum_percentage
        if total_percentage != 100:
            messagebox.showerror("Error", "The total percentage of all metals must equal 100%.")
            return
        
        # Calculate the weight of each metal
        gold_weight = (gold_percentage / 100) * total_weight
        copper_weight = (copper_percentage / 100) * total_weight
        aluminum_weight = (aluminum_percentage / 100) * total_weight

        # Display the results in the result labels
        label_gold_result.config(text=f"Gold content: {gold_weight:.2f} grams")
        label_copper_result.config(text=f"Copper content: {copper_weight:.2f} grams")
        label_aluminum_result.config(text=f"Aluminum content: {aluminum_weight:.2f} grams")
    
    except ValueError:
        messagebox.showerror("Input Error", "Please enter valid numeric values for weight and percentages.")

# Create the main window
root = tk.Tk()
root.title("Metal Mixture Calculator")
root.geometry("400x400")

# Create and place labels and entry fields for total weight and metal percentages
label_total_weight = tk.Label(root, text="Total weight of mixture (grams):")
label_total_weight.pack(pady=10)
entry_total_weight = tk.Entry(root)
entry_total_weight.pack(pady=5)

label_gold_percentage = tk.Label(root, text="Percentage of gold (%):")
label_gold_percentage.pack(pady=10)
entry_gold_percentage = tk.Entry(root)
entry_gold_percentage.pack(pady=5)

label_copper_percentage = tk.Label(root, text="Percentage of copper (%):")
label_copper_percentage.pack(pady=10)
entry_copper_percentage = tk.Entry(root)
entry_copper_percentage.pack(pady=5)

label_aluminum_percentage = tk.Label(root, text="Percentage of aluminum (%):")import tkinter as tk
from tkinter import messagebox

# Function to calculate the weight of each metal in the mixture
def calculate_mixture():
    try:
        # Get the user inputs from the entry fields
        total_weight = float(entry_total_weight.get())
        gold_percentage = float(entry_gold_percentage.get())
        copper_percentage = float(entry_copper_percentage.get())
        aluminum_percentage = float(entry_aluminum_percentage.get())

        # Validate that the total percentage equals 100
        total_percentage = gold_percentage + copper_percentage + aluminum_percentage
        if total_percentage != 100:
            messagebox.showerror("Error", "The total percentage of all metals must equal 100%.")
            return
        
        # Calculate the weight of each metal
        gold_weight = (gold_percentage / 100) * total_weight
        copper_weight = (copper_percentage / 100) * total_weight
        aluminum_weight = (aluminum_percentage / 100) * total_weight

        # Display the results in the result labels
        label_gold_result.config(text=f"Gold content: {gold_weight:.2f} grams")
        label_copper_result.config(text=f"Copper content: {copper_weight:.2f} grams")
        label_aluminum_result.config(text=f"Aluminum content: {aluminum_weight:.2f} grams")
    
    except ValueError:
        messagebox.showerror("Input Error", "Please enter valid numeric values for weight and percentages.")

# Create the main window
root = tk.Tk()
root.title("Metal Mixture Calculator")
root.geometry("400x400")

# Create and place labels and entry fields for total weight and metal percentages
label_total_weight = tk.Label(root, text="Total weight of mixture (grams):")
label_total_weight.pack(pady=10)
entry_total_weight = tk.Entry(root)
entry_total_weight.pack(pady=5)

label_gold_percentage = tk.Label(root, text="Percentage of gold (%):")
label_gold_percentage.pack(pady=10)
entry_gold_percentage = tk.Entry(root)
entry_gold_percentage.pack(pady=5)

label_copper_percentage = tk.Label(root, text="Percentage of copper (%):")
label_copper_percentage.pack(pady=10)
entry_copper_percentage = tk.Entry(root)
entry_copper_percentage.pack(pady=5)

label_aluminum_percentage = tk.Label(root, text="Percentage of aluminum (%):")
label_aluminum_percentage.pack(pady=10)
entry_aluminum_percentage = tk.Entry(root)
entry_aluminum_percentage.pack(pady=5)

# Create and place a button to trigger the calculation
button_calculate = tk.Button(root, text="Calculate", command=calculate_mixture)
button_calculate.pack(pady=20)

# Create and place labels to display the results
label_gold_result = tk.Label(root, text="")
label_gold_result.pack(pady=5)

label_copper_result = tk.Label(root, text="")
label_copper_result.pack(pady=5)

label_aluminum_result = tk.Label(root, text="")
label_aluminum_result.pack(pady=5)

# Run the Tkinter event loop
root.mainloop()￼Enter
