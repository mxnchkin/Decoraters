# Decoraters
import tkinter
from tkinter import *
window = tkinter.Tk()
label_title = tkinter.Label(window, font=("Arial", 25), text="The Decorators").grid(row=0, column=1)

#name
label_name = tkinter.Label(window, font=("Arial", 12), text="Name :").grid(row=1, column=0)
tkinter.Entry(window).grid(row=1, column=1)

#phone number
label_phone = tkinter.Label(window, font=("Arial", 12), text="Phone Number :").grid(row=2, column=0)
tkinter.Entry(window).grid(row=2, column=1)

#address
label_address = tkinter.Label(window, font=("Arial", 12), text="Address :").grid(row=3, column=0)
tkinter.Entry(window).grid(row=3, column=1)

#email
label_email = tkinter.Label(window, font=("Arial", 12), text="Email :").grid(row=4, column=0)
tkinter.Entry(window).grid(row=4, column=1)

#height
label_height = tkinter.Label(window, font=("Arial", 12), text = "Height :").grid(row=1, column=2)
height = tkinter.Entry(window)
height.grid(row = 1, column = 3)

#length of 4 walls
label_length = tkinter.Label(window, font=("Arial", 12), text="Length of walls :").grid(row=3, column=2)
label_length_1 = tkinter.Label(window, font=("Arial", 12), text="Wall 1 :").grid(row=4, column=2)
label_length_2 = tkinter.Label(window, font=("Arial", 12), text="Wall 2 :").grid(row=5, column=2)
label_length_3 = tkinter.Label(window, font=("Arial", 12), text="Wall 3 :").grid(row=6, column=2)
label_length_4 = tkinter.Label(window, font=("Arial", 12), text="Wall 4 :").grid(row=7, column=2)
length = tkinter.Entry(window)
length.grid(row=4, column=3)
length = tkinter.Entry(window)
length.grid(row=5, column=3)
length = tkinter.Entry(window)
length.grid(row=6, column=3)
length = tkinter.Entry(window)
length.grid(row=7, column=3)

#line 2 is empty
label_name = tkinter.Label(window, text = " ").grid(row=2, column=2)
#paint type
def sel_paint():
    selection = "you selected this option" + str(paint_type.get())
    print(selection)

paint_type = IntVar()
label_paint_type = tkinter.Label(window, font=("Arial"), text = "Paint Type").grid(row=10, column=0)
rb1 = Radiobutton(window, text="Luxury", variable=paint_type, value=1, command=sel_paint)
rb1.grid(row=10, column=1)
rb1 = Radiobutton(window, text="Standard", variable=paint_type, value=2, command=sel_paint)
rb1.grid(row=13, column=1)
rb1 = Radiobutton(window, text="Economy", variable=paint_type, value=3, command=sel_paint)
rb1.grid(row=15, column=1)

#undercoat
CheckVar1 = IntVar()
label_height = tkinter.Label(window, font=("Arial", 12), text = "Undercoat :").grid(row=6, column=0)
tkinter.Checkbutton(window, text = "required", variable = CheckVar1, onvalue = 1, offvalue = 0).grid(row=6, column=1)

window.mainloop()
