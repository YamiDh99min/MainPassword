from tkinter import *
from random import randint

root = Tk()
root.title('Strong Password Generator')
root.geometry("500x300")

my_password = chr(randint(45, 113))

#Label Frame
xText = LabelFrame(root, text="How Many Character is there?")
xText.pack(pady=20)

#Create Entry Box to Designate Number of Character
my_entry = Entry(xText, font("Roboto", 24))
my_entry.pack(pady=20, padx=20)

#Create Entry Box for our Returned Password
pw_entry = Entry(root, text='', font=("Helvetica", 24))
pw_entry.pack(pady=20)

#Create a frome for our Buttons
my_frame = Frame(root)
my_frame.pack(pady=20)

#Create our Buttons
my_button = Button(my_frame, text="Generate Strong Password", command=new_rand)

my_button.grid(row=0, column=0, padx=10)

clip_button = Button(my_frame, text="Copy to Clipboard", command=clipper)

clip_button.grid(row=0, column=1, padx=10)
root.mainloop()
