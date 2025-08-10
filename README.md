# Digital-Clock
import tkinter as tk   # tkinter model used to create GUI in python
from time import strftime   #time module to import strftime() function to format time & date into human readable strings

root = tk.Tk()    #creating a root window to dispaly time and date

root.title("Digital Clock")    #title() Sets the window’s title bar text


def time():
    str = strftime('%H:%M:%S %p \n %D')  #strftime() to fetch current date and time

    label.config(text=str)  #config() method to assign str variable to text attribute

    label.after(1000,time)  #Schedules the time() function to run again after 1000 milliseconds (1 second).

label = tk.Label(root, font=('calibri', 50, 'bold'), background='yellow', foreground='black')
# Customizes font, size, background color, and text color

#now we need to pack label into root window
#pack() arrange elements into window
label.pack(anchor='center')

time() # execute time()
root.mainloop()  # keeps the window open and responsive
