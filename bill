from tkinter import *

root = Tk()
root.geometry("1000x500")
root.title("Bill Management")
root.resizable(False, False)

def Reset():
    entry_dosa.delete(0, END)
    entry_cookies.delete(0, END)
    entry_Tea.delete(0, END)
    entry_coffee.delete(0, END)
    entry_juice.delete(0, END)
    entry_pancakes.delete(0, END)
    entry_eggs.delete(0, END)
    Total_bill.set("")

def Total():
    try: a1 = int(dosa.get())
    except: a1 = 0
    try: a2 = int(cookies.get())
    except: a2 = 0
    try: a3 = int(Tea.get())
    except: a3 = 0
    try: a4 = int(coffee.get())
    except: a4 = 0
    try: a5 = int(juice.get())
    except: a5 = 0
    try: a6 = int(pancakes.get())
    except: a6 = 0
    try: a7 = int(eggs.get())
    except: a7 = 0

    # Define cost of each item
    c1 = 60 * a1
    c2 = 30 * a2
    c3 = 7 * a3
    c4 = 100 * a4
    c5 = 20 * a5
    c6 = 15 * a6
    c7 = 7 * a7

    totalcost = c1 + c2 + c3 + c4 + c5 + c6 + c7
    string_bill = f"Rs. {totalcost:.2f}"
    Total_bill.set(string_bill)

# Title Label
Label(root, text="BILL MANAGEMENT", bg="blue", fg="white", font=("calibri", 33), width="300", height="2").pack()

# Menu Card Frame
f = Frame(root, bg="lightgreen", highlightbackground="black", highlightthickness=1, width=300, height=370)
f.place(x=10, y=118)

Label(f, text="Menu", font=("Gabriola", 40, "bold"), fg="black", bg="lightgreen").place(x=80, y=0)
menu_items = [
    "Dosa....... Rs.60/plate",
    "Cookies....Rs.30/plate",
    "Tea........ Rs.7/cup",
    "Coffee..... Rs.100/cup",
    "Juice...... Rs.20/glass",
    "Pancakes...Rs.15/pack",
    "Eggs....... Rs.7/egg"
]
for idx, item in enumerate(menu_items, start=1):
    Label(f, font=("Lucida Calligraphy", 15, "bold"), text=item, fg="black", bg="lightgreen").place(x=10, y=50 + 30 * idx)

# Bill Frame
f2 = Frame(root, bg="lightyellow", highlightbackground="black", highlightthickness=1, width=300, height=370)
f2.place(x=690, y=118)

Label(f2, text="Bill", font=('calibri', 20), bg="lightyellow").place(x=120, y=10)

# Entry and Button Frame
f1 = Frame(root, bd=5, height=370, width=300, relief=RAISED)
f1.place(x=340, y=118)

dosa = StringVar()
cookies = StringVar()
Tea = StringVar()
coffee = StringVar()
juice = StringVar()
pancakes = StringVar()
eggs = StringVar()
Total_bill = StringVar()

# Labels and Entry Widgets
items = [("Dosa", dosa), ("Cookies", cookies), ("Tea", Tea), ("Coffee", coffee), ("Juice", juice), ("Pancakes", pancakes), ("Eggs", eggs)]
for idx, (item, var) in enumerate(items, start=1):
    Label(f1, font=("aria", 20, 'bold'), text=item, width=12, fg="blue4").grid(row=idx, column=0)
    Entry(f1, font=("aria", 20, 'bold'), textvariable=var, bd=6, width=8, bg="lightpink").grid(row=idx, column=1)

# Buttons
Button(f1, bd=5, fg="black", bg="lightblue", font=("ariel", 16, 'bold'), width=10, text="Reset", command=Reset).grid(row=8, column=0)
Button(f1, bd=5, fg="black", bg="lightblue", font=("ariel", 16, 'bold'), width=10, text="Total", command=Total).grid(row=8, column=1)

# Display Total Bill
entry_total = Entry(f2, font=('aria', 20, 'bold'), textvariable=Total_bill, bd=6, width=15, bg="lightgreen")
entry_total.place(x=20, y=100)

root.mainloop()
