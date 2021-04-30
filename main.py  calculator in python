from tkinter import *
from tkinter.messagebox import *
font= ('Aerial', 24,"bold")


def clear():
    ex = textField.get()
    ex = ex[0:len(ex)-1]
    textField.delete(0, END)
    textField.insert(0, ex)


def all_clear():
    textField.delete(0, END)


def click_btn_func(event):
    print("btn clicked")
    b=event.widget
    text= b['text']
    print(text)

    if text == '=':
        try:

           ex=textField.get()
           answr= eval(ex)
           textField.delete(0, END)
           textField.insert(0, answr)
        except Exception as e:
            print("ERROR",e)
            showerror("ERROR",e)
        return


    textField.insert(END, text)

window= Tk()
window.title('Calculator')
window.geometry('450x450')
# pic=PhotoImage(file='pics/cal2 img.jpg')
#
# headingLabel=Label(window,Image=pic)
# headingLabel.pack(side= TOP)

heading=Label(window, text='My Calculator', font= font)
heading.pack(side=TOP)

textField= Entry(window,font=font, justify= RIGHT)
textField.pack(side=TOP,pady=10, fill=X, padx=10 )

buttonFrame= Frame(window)
buttonFrame.pack(side=TOP)

temp=1
for i in range(0, 3):
    for j in range(0, 3):
        btn=Button(buttonFrame,text=str(temp), font=font, activebackground= 'orange',width= 4, relief= 'ridge')
        btn.grid(row=i, column=j)
        temp=temp+1
        btn.bind('<Button-1>', click_btn_func)

zeroBtn=Button(buttonFrame,text='0', font=font, activebackground= 'orange',width= 4, relief= 'ridge')
zeroBtn.grid(row=3, column=0)

dotBtn=Button(buttonFrame,text='.', font=font, activebackground= 'orange',width= 4, relief= 'ridge')
dotBtn.grid(row=3, column=1)

equalBtn =Button(buttonFrame,text='=', font=font, activebackground= 'orange',width= 4, relief= 'ridge')
equalBtn.grid(row=3, column=2)

plusBtn =Button(buttonFrame,text='+', font=font, activebackground= 'orange',width= 4, relief= 'ridge')
plusBtn.grid(row=0, column=3)

minusBtn =Button(buttonFrame,text='-', font=font, activebackground= 'orange',width= 4, relief= 'ridge')
minusBtn.grid(row=1, column=3)

multBtn =Button(buttonFrame,text='*', font=font, activebackground= 'orange',width= 4, relief= 'ridge')
multBtn.grid(row=2, column=3)

divnBtn =Button(buttonFrame,text='/', font=font, activebackground= 'orange',width= 4, relief= 'ridge')
divnBtn.grid(row=3, column=3)

clrBtn =Button(buttonFrame,text='<<',font=font, activebackground= 'orange',width=9, relief= 'ridge',command= clear)
clrBtn.grid(row=4, column=0,columnspan=2)

allClearBtn =Button(buttonFrame,text='AC', font=font, activebackground= 'orange',width=9, relief= 'ridge', command= all_clear)
allClearBtn.grid(row=4, column=2,columnspan=2)

equalBtn.bind('<Button-1>', click_btn_func)
plusBtn.bind('<Button-1>', click_btn_func)
minusBtn.bind('<Button-1>', click_btn_func)
divnBtn.bind('<Button-1>', click_btn_func)
multBtn.bind('<Button-1>', click_btn_func)
clrBtn.bind('<Button-1>', click_btn_func)
allClearBtn.bind('<Button-1>', click_btn_func)
dotBtn.bind('<Button-1>', click_btn_func)

window.mainloop()
