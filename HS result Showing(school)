from tkinter import *
from tkinter.messagebox import askokcancel
import openpyxl
import os
win=Tk()
width=600
height=680
sys_width=win.winfo_screenwidth()
sys_height=win.winfo_screenheight()
c_x=int(sys_width/2-width/2)
c_y=int(sys_height/2-height/2)
win.geometry(f"{width}x{height}+{c_x}+{c_y}")
win.resizable(False,False)
win.title("School")
win.config(bg="light blue")
#---------------------------------------------------------------
# Excel file create or load
file="result.xlsx"
if not os.path.exists(file):
    wb=openpyxl.Workbook()
    ws=wb.active
    ws.append(["Name","Bengali","English","Physics","Chemistry","Mathematics","Biology","Total","Percentage","Division"])
    wb.save(file)
def save_excel(row):
    wb=openpyxl.load_workbook(file)
    ws=wb.active
    ws.append(row)
    wb.save(file)
    return
#---------------------------------------------------------------
# School Name
school_name=Label(win,text="Natra High School (H.S)",font=("Bell MT",30,"bold"),bg="light blue")
school_name.place(x=20,y=20,height=60,width=600)
#---------------------------------------------------------------
# Student Name
st_name=Label(win,text="Student Name: ",font=("Bell MT",20,"bold"),bg="light blue")
st_name.place(x=10,y=100,height=60,width=200)
student=StringVar()
st_name_entry=Entry(win,font=("Bell MT",20,"bold"),bg="light blue",justify="center",textvariable=student,relief="sunken")
st_name_entry.place(x=230,y=107,height=40,width=300)
#---------------------------------------------------------------
# Subject Numbers Heading
subject=Label(win,text="Subject Numbers",font=("Bell MT",30,"bold"),bg="light blue")
subject.place(x=100,y=160,height=60,width=600)
#---------------------------------------------------------------
# Bengali
bengali=Label(win,text="Bengalli: ",font=("Bell MT",20,"bold"))
bengali.place(x=10,y=240,height=40,width=200)
bng=DoubleVar()
bengali1=Entry(win,font=("Times New Roman",30,"bold"),justify="center",textvariable=bng)
bengali1.place(x=230,y=240,height=40,width=300)
# English
english=Label(win,text="English: ",font=("Bell MT",20,"bold"))
english.place(x=10,y=300,height=40,width=200)
eng=DoubleVar()
english1=Entry(win,font=("Times New Roman",30,"bold"),justify="center",textvariable=eng)
english1.place(x=230,y=300,height=40,width=300)
# Physics
physics=Label(win,text="Physics: ",font=("Bell MT",20,"bold"))
physics.place(x=10,y=360,height=40,width=200)
phy=DoubleVar()
physics1=Entry(win,font=("Times New Roman",30,"bold"),justify="center",textvariable=phy)
physics1.place(x=230,y=360,height=40,width=300)
# Mathematics
mathematics=Label(win,text="Mathematics: ",font=("Bell MT",20,"bold"))
mathematics.place(x=20,y=420,height=40,width=200)
math=DoubleVar()
mathematics1=Entry(win,font=("Times New Roman",30,"bold"),justify="center",textvariable=math)
mathematics1.place(x=230,y=420,height=40,width=300)
# Chemistry
chemistry=Label(win,text="Chemistry: ",font=("Bell MT",20,"bold"))
chemistry.place(x=10,y=480,height=40,width=200)
chem=DoubleVar()
chemistry1=Entry(win,font=("Times New Roman",30,"bold"),justify="center",textvariable=chem)
chemistry1.place(x=230,y=480,height=40,width=300)
# Biology
biology=Label(win,text="Biology: ",font=("Bell MT",20,"bold"))
biology.place(x=10,y=540,height=40,width=200)
bio=DoubleVar()
biology1=Entry(win,font=("Times New Roman",30,"bold"),justify="center",textvariable=bio)
biology1.place(x=230,y=540,height=40,width=300)
#---------------------------------------------------------------
# Calculate and show data
def data():
    name=student.get()
    bengali=bng.get()
    english=eng.get()
    physics=phy.get()
    mathametics=math.get()
    chemistry=chem.get()
    biology=bio.get()
    total_number=bengali+english+physics+mathametics+chemistry+biology
    per=(total_number/500)*100
    div=""
    if per>100:
        div="Please Enter valid Number"
    elif per>=70:
        div="STAR '*'"
    elif per>=60:
        div="1st division"
    elif per>=50:
        div="2nd division"
    elif per>=40:
        div="3rd division"
    else:
        div="You are fail"
    # SAVE TO EXCEL
    save_excel([name,bengali,english,physics,chemistry,mathametics,biology,total_number,per,div])
    message_box(name,total_number,per,div)
#---------------------------------------------------------------
# Message Box
def message_box(*data):
    print1=(f"Student Name: {data[0]}\nTotal Marks: {data[1]}\nPercentage: {data[2]}\nDivision: {data[3]}")
    box=askokcancel(title="Show your Result",message=print1)
    if box:
        bt=Button(win,win.destroy())
    else:
        pass
    return
#---------------------------------------------------------------
# Button
bt=Button(win,text="Result",font=("Arial",20),relief="sunken",command=data)
bt.place(x=200,y=600,height=60,width=190)

win.mainloop()
