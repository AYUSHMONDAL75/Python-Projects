from tkinter import *
from tkinter.messagebox import showinfo
from pyexcel import*
import os
win = Tk()
def main_file():
    width=900
    height=700
    sys_width=win.winfo_screenwidth()
    sys_height=win.winfo_screenheight()
    c_x=int(sys_width/2-width/2)
    c_y=int(sys_height/2-height/2)
    win.geometry(f"{width}x{height}+{c_x}+{c_y}")
    win.resizable(False, False)
    win.title("College Admission")
    win.config(bg="Yellow")
    # ---------------------------------------------------------------------------------------
    # Outer Frame
    form_frame=Frame(win, bg="light blue",bd=4,relief="groove")
    form_frame.place(x=10,y=10,width=880,height=680)
    # -------------------------------------------------------------------------------------------
    # College name & address
    college_name=Label(form_frame,text="St. Thomas' College of Engineering and Technology",font=("Lucida Calligraphy", 22, "bold"),bg="light blue",fg="red")
    college_name.place(x=12,y=5)
    college_address=Label(form_frame,text="Kidderpore 4, Diamond Harbour Road, Kolkata - 700023 (+91 1234567890)",font=("Bookman Old Style", 15,"bold"),bg="light blue")
    college_address.place(x=50, y=50)
    # --------------------------------------------------------------------------------------
    # Separator line
    separator=Frame(form_frame,bg="black",height=2)
    separator.place(x=15, y=90, width=840)
    # ------------------------------------------------------------------------------------------
    # Student Information Title
    title = Label(form_frame,text="Student Information",font=("Bradley Hand ITC",30,"bold","underline"),bg="light blue",fg="dark blue")
    title.place(x=270, y=95)
    # ---------------------------Student details--------------------------------------------------------------------
    # Student Name
    St_name = Label(form_frame, text="Name:",font=("Bell MT",18,"bold"),bg="light blue")
    St_name.place(x=20, y=150)
    st_name_var=StringVar()
    St_name_entry = Entry(form_frame,textvariable=st_name_var,font=("Calisto MT", 16),bd=1,relief="ridge",bg="light blue",justify="center")
    St_name_entry.place(x=200, y=150, width=668)
    #----------------------------Parante's Name----------------------------------------------------------------------
    # Father's Name
    St_fa_name = Label(form_frame, text="Father's Name:",font=("Bell MT",18,"bold"),bg="light blue")
    St_fa_name.place(x=20,y=200)
    st_fa_var=StringVar()
    St_fa_name_entry=Entry(form_frame, textvariable=st_fa_var,font=("Calisto MT",16),bd=1,relief="ridge",bg="light blue",justify="center")
    St_fa_name_entry.place(x=200,y=200,width=668)
    # Mother's Name
    St_ma_name = Label(form_frame, text="Mother's Name:",font=("Bell MT",18,"bold"),bg="light blue")
    St_ma_name.place(x=20, y=250)
    st_ma_var=StringVar()
    St_ma_name_entry=Entry(form_frame,textvariable=st_ma_var,font=("Calisto MT",16),bd=1,relief="ridge",bg="light blue",justify="center")
    St_ma_name_entry.place(x=200, y=250,width=668)
    #------------------------------Phone & Email ID------------------------------------------------------------------
    # Phone Number
    St_ph_number = Label(form_frame,text="Phone Number:",font=("Bell MT",18,"bold"),bg="light blue")
    St_ph_number.place(x=20, y=300)
    st_ph_var=StringVar()
    St_ph_number_entry = Entry(form_frame,textvariable=st_ph_var,font=("Calisto MT",16),bd=1,relief="ridge",bg="light blue",justify="center")
    St_ph_number_entry.place(x=200, y=300, width=180)
    # Email ID
    St_email = Label(form_frame, text="Email Id:",font=("Bell MT", 18,"bold"),bg="light blue")
    St_email.place(x=390,y=300)
    St_email_var=StringVar()
    St_email_entry = Entry(form_frame,textvariable=St_email_var,font=("Calisto MT",16),bd=1,relief="ridge",bg="light blue",justify="center")
    St_email_entry.place(x=500, y=300, width=368)
    # Guardian Phone number
    St_gdp_ph = Label(form_frame, text="Guardian's Phone:",font=("Bell MT", 18,"bold"),bg="light blue")
    St_gdp_ph.place(x=20,y=350)
    gdp_var=StringVar()
    St_gdp_ph_entry = Entry(form_frame,textvariable=gdp_var,font=("Calisto MT", 16),bd=1,relief="ridge",bg="light blue",justify="center")
    St_gdp_ph_entry.place(x=230, y=350, width=200)
    # Date of Birth
    d_o_b=Label(form_frame,text="Date of Birth:",font=("Bell MT", 18,"bold"),bg="light blue")
    d_o_b.place(x=445,y=350)
    d_o_b_var=StringVar()
    d_o_b_entry=Entry(form_frame,textvariable=d_o_b_var,font=("Calisto MT",16),bd=1,relief="ridge",bg="light blue",justify="center")
    d_o_b_entry.place(x=600,y=350,width=180)
    #------------------------------Religion, cast & Gender-----------------------------------
    # Religion, cast & gender
    religion_list=["Hinduism","Christianity","Islam","Buddhism","Sikhism"]
    religion=Label(form_frame,text="Religion:",font=("Bell MT", 18,"bold"),bg="light blue")
    religion.place(x=20,y=400)
    religion_var=StringVar()
    religion_menu=OptionMenu(form_frame,religion_var,*religion_list)
    religion_menu.config(font=("Calisto MT", 14), bg="light blue",relief="ridge",bd=1,cursor="hand2",activebackground="lightgreen")
    religion_menu.place(x=130,y=400,width=150)
    #Caste
    cast_list=["General","OBC","SC","ST","TWD"]
    cast=Label(form_frame,text="Caste:",font=("Bell MT",18,"bold"),bg="light blue")
    cast.place(x=295,y=400)
    cast_var=StringVar()
    cast_menu=OptionMenu(form_frame,cast_var,*cast_list)
    cast_menu.config(font=("Calisto MT", 14), bg="light blue",relief="ridge",bd=1,cursor="hand2",activebackground="lightgreen")
    cast_menu.place(x=370,y=400,width=150)
    # Gender
    gender_list=["Male","Female"]
    gender=Label(form_frame,text="Gender:",font=("Bell MT",18,"bold"),bg="light blue")
    gender.place(x=535,y=400)
    gender_var=StringVar()
    gender_menu=OptionMenu(form_frame,gender_var,*gender_list)
    gender_menu.config(font=("Calisto MT", 14),bg="light blue",relief="ridge",bd=1,cursor="hand2",activebackground="lightgreen")
    gender_menu.place(x=635,y=400,width=150)
    #------------------------------------- Marks --------------------------------------------------
    # 10th Marks
    st_10th_name=Label(form_frame,text="10th Marks (%):",font=("Bell MT",18,"bold"),bg="light blue")
    st_10th_name.place(x=20,y=450)
    st_10th_var=StringVar()
    st_10th_name_entry=Entry(form_frame,textvariable=st_10th_var,font=("Calisto MT",16),bd=1,relief="ridge",bg="light blue",justify="center")
    st_10th_name_entry.place(x=205,y=450,width=100)
    # 12th Marks
    st_12th_name=Label(form_frame,text="12th Marks (%):",font=("Bell MT", 18,"bold"),bg="light blue")
    st_12th_name.place(x=320,y=450)
    st_12th_var=StringVar()
    st_12th_name_entry=Entry(form_frame,textvariable=st_12th_var,font=("Calisto MT",16),bd=1,relief="ridge",bg="light blue",justify="center")
    st_12th_name_entry.place(x=505,y=450,width=100)
    #WBJEE/JEE rank
    st_rank_name=Label(form_frame,text="Rank:",font=("Bell MT", 18,"bold"),bg="light blue")
    st_rank_name.place(x=620,y=450)
    st_rank_var=StringVar()
    st_rank_name_entry=Entry(form_frame,textvariable=st_rank_var,font=("Calisto MT",16),bd=1,relief="ridge",bg="light blue",justify="center")
    st_rank_name_entry.place(x=695,y=450,width=100)
    #--------------------------------------------------------------------------------------
    # Address
    st_add=Label(form_frame,text="Address:",font=("Bell MT", 18,"bold"),bg="light blue")
    st_add.place(x=20,y=500)
    st_add_var=StringVar()
    st_add_entry=Entry(form_frame,textvariable=st_add_var,font=("Calisto MT",16),bd=1,relief="ridge",bg="light blue",justify="center")
    st_add_entry.place(x=135,y=500,width=720)
    # ------------------------------Country and State---------------------------------------------
    # Country
    country_label = Label(form_frame,text="Country:",font=("Bell MT",18,"bold"),bg="light blue")
    country_label.place(x=20, y=550)
    country_var = StringVar()
    country_list = ["India","Nepal","Bhutan","SriLanka","USA","UK"]
    country_menu = OptionMenu(form_frame, country_var,*country_list)
    country_menu.config(font=("Calisto MT", 14),bg="light blue",relief="ridge",bd=1,cursor="hand2",activebackground="lightgreen")
    country_menu.place(x=125, y=545,width=150)
    # Sate
    state_label = Label(form_frame,text="State:",font=("Bell MT",18,"bold"),bg="light blue")
    state_label.place(x=290,y=550)
    state_var = StringVar()
    state_list = ["West Bengal","Bihar","UP","Delhi","Assam","Punjab","Odisha"]
    state_menu = OptionMenu(form_frame, state_var,*state_list)
    state_menu.config(font=("Calisto MT",14),bg="light blue",relief="ridge",bd=1,cursor="hand2",activebackground="lightgreen")
    state_menu.place(x=365,y=545,width=150)
    # --------------------------------------------------------------------------------------
    # Department
    St_dep = Label(form_frame,text="Department:",font=("Bell MT",18,"bold"),bg="light blue")
    St_dep.place(x=20,y=600)
    dep_aiml = IntVar()
    dep_cse = IntVar()
    dep_it = IntVar()
    dep_ece = IntVar()
    dep_ee=IntVar()
    c1 = Checkbutton(form_frame,text="AIML",font=("Bell MT",18,"bold"),bg="light blue",variable=dep_aiml,cursor="hand2",activebackground="lightblue")
    c1.place(x=200,y=600)
    c2 = Checkbutton(form_frame,text="CSE",font=("Bell MT",18,"bold"),bg="light blue",variable=dep_cse,cursor="hand2",activebackground="lightblue")
    c2.place(x=310,y=600)
    c3 = Checkbutton(form_frame,text="IT",font=("Bell MT",18,"bold"),bg="light blue",variable=dep_it,cursor="hand2",activebackground="lightblue")
    c3.place(x=400,y=600)
    c4 = Checkbutton(form_frame,text="ECE",font=("Bell MT",18,"bold"),bg="light blue",variable=dep_ece,cursor="hand2",activebackground="lightblue")
    c4.place(x=475,y=600)
    c5 = Checkbutton(form_frame,text="EE",font=("Bell MT",18,"bold"),bg="light blue",variable=dep_ee,cursor="hand2",activebackground="lightblue")
    c5.place(x=570,y=600)
    #----------------------------------------------------------------------------------
    #date from user
    def save():
        file_name="college_admission.xlsx"
    #for department data
        department=""
        if dep_aiml.get()==1:department="AIML"
        elif dep_cse.get()==1:department="CSE"
        elif dep_it.get()==1:department="IT"
        elif dep_ece.get()==1:department="ECE"
        elif dep_ee.get()==1:department="EE"
    #for others details
        row=[
            st_name_var.get(),st_fa_var.get(),st_ma_var.get(),st_ph_var.get(),
            St_email_var.get(),gdp_var.get(),d_o_b_var.get(),religion_var.get(),
            cast_var.get(),gender_var.get(),st_10th_var.get(),st_12th_var.get(),
            st_rank_var.get(),st_add_var.get(),country_var.get(),state_var.get(),
            department
        ]
        header=["Name","Father's Name","Mother's Name","Phone","Email","Guardian's phone",
            "DOB","Religion","cast","gender","10th%","12th%","Rank","Address","Country","State","Department"]
        if not os.path.exists(file_name):
            sheet=Sheet([header,row])
            sheet.save_as(file_name)
        else:
            sheet=get_sheet(file_name=file_name)
            sheet.row+=row
            sheet.save_as(file_name)
        return
    # ---------------------------# For  Submit & Exit Button -------------------------------
    # Function for Exit
    def exi_t():
        win.destroy()
        return
    # Function for message
    def submit():
        showinfo(title="Submit",message="Congratulations! Your form has been submitted.")
        return
    bt_submit=Button(form_frame,text="Submit",font=("Viner Hand ITC",12,"bold"),fg="green",bg="light blue",relief="groove",bd=3,cursor="hand2",command=lambda:[save(),submit()],activebackground="green")
    bt_submit.place(x=785,y=620)
    bt_exit=Button(win,text="Exit",font=("Viner Hand ITC",9,"bold"),fg="red",bg="light blue",relief="groove",bd=3,command=exi_t,cursor="hand2",activebackground="red")
    bt_exit.place(x=20,y=650)
    return
#----------------------------------------------------------------------------------------------------------
#main window
win.title("STCET")
width=650
height=400
sys_width=win.winfo_screenwidth()
sys_height=win.winfo_screenheight()
c_x=int(sys_width/2-width/2)
c_y=int(sys_height/2-height/2)
win.geometry(f"{width}x{height}+{c_x}+{c_y}")
win.resizable(False,False)
win.config(bg="lightgreen")
main_file1=Label(win, text="ST. THOMAS COLLEGE OF ENGINEERING AND TECHNOLOGY", font=("Bell MT",15,"bold"),fg="red",bg="lightgreen")
main_file1.pack(pady=20)
main_file2=Label(win, text="Address: 4, Diamond Harbour Road, Kidderpore, Kolkata - 700023", font=("Georgia",14),fg="blue",bg="lightgreen")
main_file2.pack(pady=2)
main_file3=Label(win, text="Admission Form", font=("Bookman Old Style", 17,"bold","underline"),fg="darkblue",bg="lightgreen")
main_file3.pack(pady=5)
main_file_button=Button(win, text="Click to fill up the form", font=("Bahnschrift Light",10,"bold"),command=main_file,bd=3,bg="lightgreen",cursor="hand2",relief="groove",activebackground="blue",activeforeground="brown")
main_file_button.pack(pady=15)
#..............................................................................................
win.mainloop()
