# tela-de-registro
Uma tela de registro que pede o nome,email e senha do usuário.
from tkinter import*
from time import sleep



janela=Tk()
janela.title("Portal de alunos")
janela.geometry("490x560+400+154")
janela.resizable(width=1,height=1)

def novajanela():
    janela.destroy()
    sleep(0.3)
    master=Tk()
    master.title("Nova janela criada")
    master.geometry("490x560+400+154")
    
esconda_senha=StringVar()
texto1=Label(janela,text="Registro de usuarios",padx=100,pady=100,font=("verdana",10,"bold italic"))
texto1.grid(column=0,row=0)
en_token=Entry(janela,bd=2,font=("Calibri",15),justify=CENTER)
nome=Label(janela,text="Usuario",font=("Arial",10,"bold italic"))
nome.grid(column=0,row=1)
hum=Entry(janela,text=" ")
hum.grid(column=0,row=2)
texto2=Label(janela,text="Email",font=("Arial",10,"bold italic"))
texto2.grid(column=0,row=3)
hm=Entry(janela,bd=2,font=("Calibri",15),justify=CENTER)
hm.grid(column=0,row=4)
texto3=Label(janela,text="Id token",font=("Arial",10,"bold italic"))
texto3.grid(column=0,row=5)
an=Entry(janela,bd=2,font=("Calibri",15),justify=CENTER)
an.place(width=395,height=45,x=49,y=138)
an.grid(column=0,row=6)
texto4=Label(janela,text="Senha",font=("Arial",10,"bold italic"))
texto4.grid(column=0,row=5)
am=Entry(janela,textvariable=esconda_senha,show="*",bd=2,font=("Calibri",15),justify=CENTER)
am.place(width=392,height=45,x=49,y=244)
am.grid(column=0,row=6)
bt1=Button(janela,text="Entrar",command=novajanela)
bt1.grid(column=0,row=7)
janela.mainloop()
