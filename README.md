# Final_Project

import tkinter as tk


def main():
    disp = tk.Tk()
    disp.title("SOLUTION")
    disp.geometry("400x200")
    message_label = tk.Label(disp, text = "I am here")
    message_label.pack()
    result = tk.Label(disp, text = "Still here")
    result.pack()
    entry = tk.Entry(disp)
    entry.pack()

    
 
       

    def input():
        num = int(entry.get())
        fac = factorial_by_recursion(num)
        sum = "The factorial of " + str(num) + " will be: " + str(fac)
        value = tk.Label(disp, text = sum)
        value.pack()

    def factorial_by_recursion(num):
        if num == 0:
            return 1
        else:
            return num * factorial_by_recursion(num-1)

    
    cal = tk.Button(disp, text = "hit me", command = input)
    cal.pack()



    disp.mainloop()


main()
