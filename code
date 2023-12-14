from tkinter import*
from random import randint


root = Tk()
root.title('PASSWORD GENERATOR')
root.geometry("500x300")

my_password = chr(randint(33,126))

def new_rand():
    pw_entry.delete(0,END)
    pw_length = int(my_entry.get())
    my_password = ''
    for x in range(pw_length):
        my_password+=chr(randint(33,126))
    pw_entry.insert(0,my_password)

def clear_entry():
    my_entry.delete(0, END)
    pw_entry.delete(0,END)

def clipper():
    root.clipboard_clear()
    root.clipboard_append(pw_entry.get())

Lf=LabelFrame(root,text="How Many Characters")
Lf.pack(pady=20)

my_entry = Entry(Lf,font=("Ariel",26))
my_entry.pack(pady=20,padx=20)

pw_entry = Entry(root,text='',font=("Ariel",26),bd=0,bg="systembuttonface")
pw_entry.pack(pady=20)

my_frame = Frame(root)
my_frame.pack(pady=20)


my_button = Button(my_frame,text="Generate Strong Password",command=new_rand)
my_button.grid(row=0,column=0,padx=10)

clear_button = Button(root, text="Clear", command=clear_entry)
clear_button.pack()

clip_button = Button(my_frame,text="copy to clipboard",command=clipper)
clip_button.grid(row=0,column=1,padx=10)

root.mainloop()
 