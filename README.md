# python-project

from tkinter import *
from PIL import ImageTk,Image
from tkinter import messagebox
from tkinter.filedialog import asksaveasfile
from tkinter.filedialog import askopenfile
import random
 
def raise_frame(f):
    f.tkraise()
 
def finish():
    r.destroy()
    
def fr1():
    raise_frame(Fr1)
def fr2():
    raise_frame(Fr2)
def fr3():
    raise_frame(Fr3)
def fr4():
    raise_frame(Fr4)
def fr5():
    raise_frame(Fr5)
def fr6():
    raise_frame(Fr6)
def fr7():
    raise_frame(Fr7)
def fr8():
    raise_frame(Fr8)
def fr9():
    raise_frame(Fr9)
def fr10():
    raise_frame(Fr10)
def fr11():
    raise_frame(Fr11)
def fr12():
    raise_frame(Fr12)

#Encryption Calculations---------------------------------------------------------------------
tik=0
def fun1():
    global values1,tik
    values1 = ''
    if(tik==0):
        tik=1
        t1=e1.get()
        n=len(t1)
        if(n!=0):

            for i in range(len(t1)):
                z2=ord(t1[i])
                values1+=str(z2)+' '

        v1.set(values1)
    else:
        messagebox.showinfo('MessageBox','Please enter plain text  ')
def fun2():
    global values2,tik
    values2 = ''
    if(tik==1):
        tik=2    
        t2=e2.get()
        n=len(t2)
        if(n!=0):
            for i in range(len(t2)):
                z2=ord(t2[i])
                values2+=str(z2)+' '
        v2.set(values2)
    else:
        messagebox.showinfo('MessageBox','Please enter key value ')
def fun3():
    global values1,values2,dec,tik
    if(tik==2):
        tik=3
        values1=values1.split(' ')
        values1=values1[:-1]
        values2=values2.split(' ')
        values2=values2[:-1]
        a=values1
        b=values2
        dec=''
        for i in range(len(a)):
            dec+= str(int(a[i])*int(b[i]))+' '
        v3.set(dec)
    else:
        messagebox.showinfo('MessageBox','Please hit the previous button ')
def D8B(a):
    bnr = bin(a).replace('0b','')
    x = bnr[::-1] 
    while len(x) < 16:
        x += '0'
    bnr = x[::-1]
    return bnr
def fun4():
    global dec,binary1,tik
    if(tik==3):
        tik=4
        dec=dec.split(' ')
        dec=dec[:-1]
        binary1= ''
        for i in range(len(dec)):
            binary1+=str(D8B(int(dec[i])))+' '
        v4.set(binary1)
    else:
        messagebox.showinfo('MessageBox','Please hit the previous button ')
#==========================================Encryption 2 page Calculations ==================================#
def MATRIX(a,x1,y1,n):
   
    a1=''
    for i in range(len(a)):
        a1+=a[i]+' '
        if((i+1)%4==0):
            a1+='\n'
    a1=a1[:-1]
    if((n+1)==1):
        v5.set(a1)
        l3= Label(Fr7,textvariable= v5, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==2):
        v6.set(a1)
        l3= Label(Fr7,textvariable= v6, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==3):
        v7.set(a1)
        l3= Label(Fr7,textvariable= v7, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==4):
        v8.set(a1)
        l3= Label(Fr7,textvariable= v8, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==5):
        v9.set(a1)
        l3= Label(Fr7,textvariable= v9, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==6):
        v10.set(a1)
        l3= Label(Fr7,textvariable= v10, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==7):
        v11.set(a1)
        l3= Label(Fr7,textvariable= v11, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==8):
        v12.set(a1)
        l3= Label(Fr7,textvariable= v12, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==9):
        v13.set(a1)
        l3= Label(Fr7,textvariable= v13, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==10):
        v14.set(a1)
        l3= Label(Fr7,textvariable= v14, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)

def MATRIXD(a,x1,y1,n):
   
    a1=''
    for i in range(len(a)):
        a1+=a[i]+' '
        if((i+1)%4==0):
            a1+='\n'
    a1=a1[:-1]
    if((n+1)==1):
        v5.set(a1)
        l3= Label(Fr10,textvariable= v5, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==2):
        v6.set(a1)
        l3= Label(Fr10,textvariable= v6, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==3):
        v7.set(a1)
        l3= Label(Fr10,textvariable= v7, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==4):
        v8.set(a1)
        l3= Label(Fr10,textvariable= v8, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==5):
        v9.set(a1)
        l3= Label(Fr10,textvariable= v9, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==6):
        v10.set(a1)
        l3= Label(Fr10,textvariable= v10, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==7):
        v11.set(a1)
        l3= Label(Fr10,textvariable= v11, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==8):
        v12.set(a1)
        l3= Label(Fr10,textvariable= v12, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==9):
        v13.set(a1)
        l3= Label(Fr10,textvariable= v13, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==10):
        v14.set(a1)
        l3= Label(Fr10,textvariable= v14, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)

def MT(a):
    t=''
    
    a1=a[0]
    a2=a[1]
    a3=a[2]
    a4=a[3]
    a1=a1.replace(' ','')
    a2=a2.replace(' ','')
    a3=a3.replace(' ','')
    a4=a4.replace(' ','')

        
    for j in range(4):
            t+=str(a1[j]+a2[j]+a3[j]+a4[j])+'\n'
 

    #print(t)
    return  t

def B2D(binary):
    binary1 = binary
    decimal, i, n = 0, 0, 0
    while(binary != 0):
        dec = binary % 10
        decimal = decimal + dec * pow(2, i)
        binary = binary//10
        i += 1
    return(decimal)    
D=''
def TRANS(a,x1,y1,n):
    global D
    a1=''
    for i in range(len(a)):
        a1+=a[i]
        if((i+1)%4==0):
            a1+='\n'
    a1=a1[:-1]

    a=a1.split('\n')
    
    a1=MT(a)
    a1=a1[:-1]
    
    if((n+1)==1):
        v15.set(a1)
        A1=a1.split('\n')
        
        D+=str(B2D(int(A1[0])))+' '
        D+=str(B2D(int(A1[1])))+' '
        D+=str(B2D(int(A1[2])))+' '
        D+=str(B2D(int(A1[3])))+' '
        
        l3= Label(Fr7,textvariable= v15, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==2):
        v16.set(a1)
        A1=a1.split('\n')
        
        D+=str(B2D(int(A1[0])))+' '
        D+=str(B2D(int(A1[1])))+' '
        D+=str(B2D(int(A1[2])))+' '
        D+=str(B2D(int(A1[3])))+' '

        l3= Label(Fr7,textvariable= v16, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==3):
        v17.set(a1)
        A1=a1.split('\n')
        
        D+=str(B2D(int(A1[0])))+' '
        D+=str(B2D(int(A1[1])))+' '
        D+=str(B2D(int(A1[2])))+' '
        D+=str(B2D(int(A1[3])))+' '
        
        l3= Label(Fr7,textvariable= v17, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==4):
        v18.set(a1)
        A1=a1.split('\n')
        
        D+=str(B2D(int(A1[0])))+' '
        D+=str(B2D(int(A1[1])))+' '
        D+=str(B2D(int(A1[2])))+' '
        D+=str(B2D(int(A1[3])))+' '

        l3= Label(Fr7,textvariable= v18, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==5):
        v19.set(a1)
        A1=a1.split('\n')
        
        D+=str(B2D(int(A1[0])))+' '
        D+=str(B2D(int(A1[1])))+' '
        D+=str(B2D(int(A1[2])))+' '
        D+=str(B2D(int(A1[3])))+' '

        l3= Label(Fr7,textvariable= v19, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==6):
        v20.set(a1)
        A1=a1.split('\n')
        
        D+=str(B2D(int(A1[0])))+' '
        D+=str(B2D(int(A1[1])))+' '
        D+=str(B2D(int(A1[2])))+' '
        D+=str(B2D(int(A1[3])))+' '

        l3= Label(Fr7,textvariable= v20, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==7):
        v21.set(a1)
        A1=a1.split('\n')
        
        D+=str(B2D(int(A1[0])))+' '
        D+=str(B2D(int(A1[1])))+' '
        D+=str(B2D(int(A1[2])))+' '
        D+=str(B2D(int(A1[3])))+' '

        l3= Label(Fr7,textvariable= v21, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==8):
        v22.set(a1)
        A1=a1.split('\n')
        
        D+=str(B2D(int(A1[0])))+' '
        D+=str(B2D(int(A1[1])))+' '
        D+=str(B2D(int(A1[2])))+' '
        D+=str(B2D(int(A1[3])))+' '

        l3= Label(Fr7,textvariable= v22, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==9):
        v23.set(a1)
        A1=a1.split('\n')
        
        D+=str(B2D(int(A1[0])))+' '
        D+=str(B2D(int(A1[1])))+' '
        D+=str(B2D(int(A1[2])))+' '
        D+=str(B2D(int(A1[3])))+' '
        l3= Label(Fr7,textvariable= v23, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==10):
        v24.set(a1)
        A1=a1.split('\n')
        
        D+=str(B2D(int(A1[0])))+' '
        D+=str(B2D(int(A1[1])))+' '
        D+=str(B2D(int(A1[2])))+' '
        D+=str(B2D(int(A1[3])))+' '
        l3= Label(Fr7,textvariable= v24, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
def TRANSD(a,x1,y1,n):
    global D
    a1=''
    for i in range(len(a)):
        a1+=a[i]
        if((i+1)%4==0):
            a1+='\n'
    a1=a1[:-1]

    a=a1.split('\n')
    
    a1=MT(a)
    a1=a1[:-1]
    
    if((n+1)==1):
        v15.set(a1)
        A1=a1.split('\n')
        
        D+=str(B2D(int(A1[0]+A1[1]+A1[2]+A1[3])))+' '
        
        l3= Label(Fr10,textvariable= v15, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==2):
        v16.set(a1)
        A1=a1.split('\n')

        D+=str(B2D(int(A1[0]+A1[1]+A1[2]+A1[3])))+' '
        
        l3= Label(Fr10,textvariable= v16, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==3):
        v17.set(a1)
        A1=a1.split('\n')
        
        D+=str(B2D(int(A1[0]+A1[1]+A1[2]+A1[3])))+' '
         
        l3= Label(Fr10,textvariable= v17, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==4):
        v18.set(a1)
        A1=a1.split('\n')
        
        D+=str(B2D(int(A1[0]+A1[1]+A1[2]+A1[3])))+' '
        
        l3= Label(Fr10,textvariable= v18, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==5):
        v19.set(a1)
        A1=a1.split('\n')
        
        D+=str(B2D(int(A1[0]+A1[1]+A1[2]+A1[3])))+' '
        
        l3= Label(Fr10,textvariable= v19, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==6):
        v20.set(a1)
        A1=a1.split('\n')
        
        D+=str(B2D(int(A1[0]+A1[1]+A1[2]+A1[3])))+' '
        
        l3= Label(Fr10,textvariable= v20, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==7):
        v21.set(a1)
        A1=a1.split('\n')
        
        D+=str(B2D(int(A1[0]+A1[1]+A1[2]+A1[3])))+' '

        l3= Label(Fr10,textvariable= v21, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==8):
        v22.set(a1)
        A1=a1.split('\n')
        
        D+=str(B2D(int(A1[0]+A1[1]+A1[2]+A1[3])))+' '
        
        l3= Label(Fr10,textvariable= v22, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==9):
        v23.set(a1)
        A1=a1.split('\n')
        
        D+=str(B2D(int(A1[0]+A1[1]+A1[2]+A1[3])))+' '
        
        l3= Label(Fr10,textvariable= v23, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
    if((n+1)==10):
        v24.set(a1)
        A1=a1.split('\n')
        
        D+=str(B2D(int(A1[0]+A1[1]+A1[2]+A1[3])))+' '
        

        l3= Label(Fr10,textvariable= v24, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=6,height=4,).place(x = x1,y=y1,)
        
def fun5():
    global binary1,binary2,tik
    if(tik==4):
        tik=5
        binary=binary1.split(' ')
        binary=binary[:-1]
        binary2=binary

        x=180
        y=130
        a=''
        for i in range(len(binary)):
            a=binary[i]
            x+=100
            MATRIX(a,x,y,i)
    else:
        messagebox.showinfo('MessageBox','Please hit the previous button ')
def fun6():
    global binary2,tik
    if(tik==5):
        tik=6
        x=180
        y=280
        a=''
        for i in range(len(binary2)):
            a=binary2[i]
            x+=100
            TRANS(a,x,y,i)
    else:
        messagebox.showinfo('MessageBox','Please hit the previous button ')
def fun7():
    global a,tik,D
    if(tik==6):
        tik=7
        v25.set(D)
    else:
        messagebox.showinfo('MessageBox','Please hit the previous button ')
#==========================================Encryption 3 page Calculations ==================================#
def fun8():
    global tik
    if(tik==7):
        tik=8
        L=len(e2.get())
        v26.set(str(L))
    else:
        messagebox.showinfo('MessageBox','Please hit the previous button ')

def fun9():
    global a,vk,tik,D,vk1,ct
    mapT=['!','0','#','$','%','&','(',')','*','+','/',';','?','@','[',':',']','^',
            '{','|','}','~','×','–','Ø','©','®','±','µ',']']
    if(tik==8):
        tik=9    
        k=len(e2.get())
        vk=''
        vk1=''
        ct=''
        D=D.split(' ')
        
        for i in range(len(D)):
            if(D[i].isnumeric()):
                x=int(k)+int(D[i])
                vk+=str(x)+' '
                vk1+=str(int(x)%32)+' '
                y=int(x)%32
                ct+=str(mapT[int(y)])
        v27.set(vk)
        D=''
    else:
        messagebox.showinfo('MessageBox','Please hit the previous button ')
def fun10():
    global vk1,tik
    if(tik==9):
        tik=10
        v28.set(vk1)
    else:
        messagebox.showinfo('MessageBox','Please hit the previous button ')
def fun11():
    global ct,tik
    if(tik==10):
        tik=11
        v29.set(ct)
    else:
        messagebox.showinfo('MessageBox','Please hit the previous button ')


def SaveCT():
    global ct,tik
    if(tik==11):
        tik=12
        f = asksaveasfile(mode='w', defaultextension=".txt")
        if f is None:
            return
        f.write(ct)
        messagebox.showinfo("message dialog box", 'CIPHER text saved successfully')
        f.close()
    else:
        messagebox.showinfo('MessageBox','Please previous button ')

def Savekeys():
    global keys,tik
    if(tik==12):
        tik=13
        f = asksaveasfile(mode='w', defaultextension=".txt")
        if f is None:
            return
        f.write(e2.get())
        messagebox.showinfo("message dialog box", 'plain text saved successfully')
        f.close()
    else:
        messagebox.showinfo('MessageBox','Please previous button ')
#Decryption Calculations page-1---------------------------------------------------------------------
kit=0
def OpenCode():
    global ct
    global kit
    if(kit==0):
        kit=1
        file=askopenfile(mode='r',filetypes=[('All files','*.txt')])
        if file is not None:
            ct=file.read() 
        v30.set(ct)
    else:
        messagebox.showinfo('MessageBox','Please previous button ')
def fun12():
    global ct,kit,ctasci

    mapT=['!','0','#','$','%','&','(',')','*','+','/',';','?','@','[',':',']','^',
            '{','|','}','~','×','–','Ø','©','®','±','µ',']']
    if(kit==1):
        kit=2
        ctasci=''
        for i in range(len(ct)):
            ctasci+=str(mapT.index(ct[i]))+' '
        v31.set(ctasci)
    else:
        messagebox.showinfo('MessageBox','Please hit the previous button ')
def OpenKey():
    global key,kit
    if(kit==2):
        kit=3
        file=askopenfile(mode='r',filetypes=[('All files','*.txt')])
        if file is not None:
            key=file.read() 
        v32.set(key)
    else:
        messagebox.showinfo('MessageBox','Please previous button ')

def fun13():
    global key,kit,k
    
    if(kit==3):
        kit=4    
        k=len(key)
        v33.set(str(k))
    else:
        messagebox.showinfo('MessageBox','Please hit the previous button ')

def fun14():
    global k,pt1,ctasci,kit,bn1
    if(kit==4):
        kit=5
        ctasci=ctasci.split(' ')
        ct=ctasci[:-1]
        pt1=''
        bn1=''
        for i in range(len(ct)):
            m=str(int(ct[i])- int(k))
            pt1+=str(int(int(m)+32)%32)+' '
            bn1+=str(D4B(int(int(m)+32)%32))+' '
            #print(str(D8B(int(int(m)+32)%32)))
        v34.set(pt1)
    else:
        messagebox.showinfo('MessageBox','Please hit the previous button ')

def D4B(a):
    bnr = bin(a).replace('0b','')
    x = bnr[::-1] 
    while len(x) < 4:
        x += '0'
    bnr = x[::-1]
    return bnr

def fun15():
    global kit,bn1
    if(kit==5):
        kit=6
        v35.set(bn1)
    else:
        messagebox.showinfo('MessageBox','Please hit the previous button ')

#Decryption Calculations page-2---------------------------------------------------------------------

def fun16():
    global kit,bn1
    global binary1,binary2

    if(kit==6):
        kit=7
        binary1=bn1
        binary1=binary1.replace(' ','')
        b=''
        
        for i in range(len(binary1)):
            b+=binary1[i]
            if((i+1)%16==0):
                b+=' '
        binary1=b
        
        binary=binary1.split(' ')
        binary=binary[:-1]
        binary2=binary

        x=180
        y=130
        a=''
        for i in range(len(binary)):
            a=binary[i]
            x+=100
            MATRIXD(a,x,y,i)
    else:
        messagebox.showinfo('MessageBox','Please hit the previous button ')

def fun17():
    global kit,binary2
    if(kit==7):
        kit=8

        x=180
        y=280
        a=''
        for i in range(len(binary2)):
            a=binary2[i]
            x+=100
            TRANSD(a,x,y,i)
    else:
        messagebox.showinfo('MessageBox','Please hit the previous button ')
def fun18():
    global kit,D
    if(kit==8):
        kit=9
        v36.set(D)
    else:
        messagebox.showinfo('MessageBox','Please hit the previous button ')

#Decryption Calculations page-3---------------------------------------------------------------------

def fun19():
    global kit,key
    if(kit==9):
        kit=10
        file=askopenfile(mode='r',filetypes=[('All files','*.txt')])
        if file is not None:
            key=file.read() 
        v37.set(key)
    else:
        messagebox.showinfo('MessageBox','Please previous button ')
        
def B2D(binary):
    binary1 = binary
    decimal, i, n = 0, 0, 0
    while(binary != 0):
        dec = binary % 10
        decimal = decimal + dec * pow(2, i)
        binary = binary//10
        i += 1
    return(decimal)

def fun20():
    global k1,kit,key,kasc
    if(kit==10):
        kit=11
        kasc=''
        for i in range(len(key)):
            kasc+=str(ord(key[i]))+' '
        v38.set(kasc)
    else:
        messagebox.showinfo('MessageBox','Please hit the previous button ')
def fun21():
    global kit,D
    if(kit==11):
        kit=12
        v39.set(D)
    else:
        messagebox.showinfo('MessageBox','Please hit the previous button ')
        
def fun22():
    global kasc,kit,D,pt
    if(kit==12):
        kit=13
        kasc=kasc.split(' ')
        kasc=kasc[:-1]
        D=D.split(' ')
        D=D[:-1]
        dec=''
        pt=''
        for i in range(len(D)):
            k=int(int(D[i])/int(kasc[i]))
            dec+=str(k)+' '
            pt+=chr(k)
        
        v40.set(dec)
    else:
        messagebox.showinfo('MessageBox','Please hit the previous button ')
def fun23():
    global kit,pt
    if(kit==13):
        kit=14    
        v41.set(pt)
    else:
        messagebox.showinfo('MessageBox','Please hit the previous button ')
#======================================================
def clearAll():
    global tik,kit
    clearE1()
    clearE2()
    clearE3()
    clearD1()
    clearD2()
    tik=0
    kit=0
def clearE1():
    global tik
    tik=0
    e1.delete(0,END)
    e2.delete(0,END)
    v1.set('')
    v2.set('')
    v3.set('')
    v4.set('')
def clearE2():
    global tik
    tik=0
    v5.set('')    
    v6.set('')
    v7.set('')
    v8.set('')
    v9.set('')
    v10.set('')
    v11.set('')    
    v12.set('')
    v13.set('')
    v14.set('')
    v15.set('')
    v16.set('')
    v17.set('')
    v18.set('')
    v19.set('')
    v20.set('')
    v21.set('')
    v22.set('')
    v23.set('')
    v24.set('')
    v25.set('')
def clearE3():
    global tik
    tik=0
    v26.set('')
    v27.set('')
    v28.set('')
def clearD1():
    global kit
    kit=0
    v29.set('')
    v30.set('')
    v31.set('')
    v32.set('')
    v33.set('')
    v34.set('')
    v35.set('')
    v36.set('')
def clearD2():
    global kit
    kit=0
    v32.set('')
    v33.set('')
    v34.set('')
    v35.set('')
    v36.set('')
    v37.set('')
    v38.set('')
    v39.set('')
    v40.set('')
def clearD3():
    global kit
    kit=0
    v37.set('')
    v38.set('')
    v39.set('')
    v40.set('')
    v41.set('')
    v42.set('')
def clearD4():
    global kit
    kit=0
    v43.set('')
    v44.set('')
    v45.set('')
    v46.set('')

r = Tk()
Fr0 = Frame(r)
Fr1 = Frame(r)
Fr2 = Frame(r)
Fr3 = Frame(r)
Fr4 = Frame(r)
Fr5 = Frame(r)
Fr6 = Frame(r)
Fr7 = Frame(r)
Fr8 = Frame(r)
Fr9 = Frame(r)
Fr10 = Frame(r)
Fr11 = Frame(r)
Fr12 = Frame(r)


Fr0.place(x = 0,y = 0,height=157, width=1300)
Fr1.place(x = 0,y = 157,height=680, width=1300)
Fr2.place(x = 0,y = 157,height=680, width=1300)
Fr3.place(x = 0,y = 157,height=680, width=1300)
Fr4.place(x = 0,y = 157,height=680, width=1300)
Fr5.place(x = 0,y = 157,height=680, width=1300)
Fr6.place(x = 0,y = 157,height=680, width=1300)
Fr7.place(x = 0,y = 157,height=680, width=1300)
Fr8.place(x = 0,y = 157,height=680, width=1300)
Fr9.place(x = 0,y = 157,height=680, width=1300)
Fr10.place(x = 0,y = 157,height=680, width=1300)
Fr11.place(x = 0,y = 157,height=680, width=1300)
Fr12.place(x = 0,y = 157,height=680, width=1300)


Fr1.config(bg='white')
Fr2.config(bg='white')
Fr3.config(bg='white')
Fr4.config(bg='white')
Fr5.config(bg='white')
Fr6.config(bg='white')
Fr7.config(bg='white')
Fr8.config(bg='white')
Fr9.config(bg='white')
Fr10.config(bg='white')
Fr11.config(bg='white')
Fr12.config(bg='white')

#Variable Declaration-----------------------------------------------------------------------------------------
v1=StringVar()
v2=StringVar()
v3=StringVar()
v4=StringVar()
v5=StringVar()
v6=StringVar()
v7=StringVar()
v8=StringVar()
v9=StringVar()
v10=StringVar()
v11=StringVar()
v12=StringVar()
v121=StringVar()
v13=StringVar()
v14=StringVar()
v15=StringVar()
v16=StringVar()
v17=StringVar()
v18=StringVar()
v19=StringVar()
v20=StringVar()
v21=StringVar()
v22=StringVar()
v23=StringVar()
v24=StringVar()
v25=StringVar()
v26=StringVar()
v27=StringVar()
v28=StringVar()
v29=StringVar()
v30=StringVar()
v31=StringVar()
v32=StringVar()
v33=StringVar()
v34=StringVar()
v35=StringVar()
v36=StringVar()
v37=StringVar()
v38=StringVar()
v39=StringVar()
v40=StringVar()
v41=StringVar()
v42=StringVar()
v43=StringVar()
v44=StringVar()
v45=StringVar()

#HeadingPage
ph1=ImageTk.PhotoImage(Image.open("logo.png"))
lab2 = Label(Fr0,image=ph1).place(x = -40, y = 0)


#----------------Home Page Fr-1 -------------------------------------------------------------------------

ph2=ImageTk.PhotoImage(Image.open("bg5.jpg"))
lab2 = Label(Fr1,image=ph2).place(x = 0, y = 0)

lab2 = Label(Fr1, justify="left",text = '''A Cryptographic Algorithm Based on ASCII and Number System
     Conversions along with A Cyclic Mathematical Function
''',
                 fg="black",bg='white', font = "TimesNewRoman 22 bold",height=3).place(x = 140,y=100)

lab2 = Label(Fr1, justify="left",text = '''
Project By  MCA  4th semester 
Name : Bendi Satya Pavan
Rno :  PG212202006
''',
                 fg="black",bg='white', font = "TimesNewRoman 11 bold",height=6).place(x = 180,y=350)

lab2 = Label(Fr1, justify="left",text = '''
Project Guide By
Sir. B.Divakar 
Assistant Professor
''',
                 fg="black",bg='white', font = "TimesNewRoman 14 bold",height=5).place(x = 720,y=350)

b1 = Button(Fr1, text = "Proceed",fg="black",bg="white",bd=5, font = "TimesNewRoman 14 bold",width=8,command = fr5).place(x = 450, y = 270)
b2 = Button(Fr1, text = "Close",fg="black",bg="white",bd=5, font = "TimesNewRoman 14 bold",width=8,command=finish).place(x = 600, y = 270)



#--------------------Abstract Page   ----Fr-2---------------------------------------------------------------------------------

ph3=ImageTk.PhotoImage(Image.open("bg5.jpg"))
lab4 = Label(Fr2,image=ph3).place(x = 0, y = 0)

lab2 = Label(Fr2, justify="left",text = '''A Cryptographic Algorithm Based on ASCII and Number System
     Conversions along with A Cyclic Mathematical Function
''',
                 fg="black",bg='white', font = "TimesNewRoman 18 bold",height=3).place(x = 220,y=10)

l1 = Label(Fr2, text = "Abstract",fg="black",font = "TimesNewRoman 16 bold",bg='white',height=1,width=10).place(x = 500,y=120)


l3= Label(Fr2, text='''

Data encryption and decryption in an efficient manner are the challenging aspects of modern
information theory. In this algorithm, the plaintext to be encrypted is converted into 
unprintable characters. For encryption, a different technique is applied based on ASCII and 
number system conversions, which makes this algorithm different from others. First, each 
character of the plaintext is converted into its equivalent ASCII (decimal). Then, using some 
matrix manipulations on the decimal, representation of each character is transformed to 5 
unprintable characters. After that, every unprintable character in the intermediate cipher text 
is further converted into a different unprintable character using a cyclic mathematical 
function. Performing three steps of processing, the final encrypted message is produced that 
gives higher level of security. 
''',
          
          fg="black",bg="white",justify=LEFT, font = "TimesNewRoman 12 bold",height=12).place(x = 250,y=180)

b8 = Button(Fr2, text = "Prev",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command = fr1).place(x = 50, y=500)
b7 = Button(Fr2, text = "Next",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command=fr3).place(x = 1050, y=500)


#--------------------Current System Page   ----Fr-3---------------------------------------------------------------------------------

ph4=ImageTk.PhotoImage(Image.open("bg5.jpg"))
lab4 = Label(Fr3,image=ph4).place(x = 0, y = 0)

lab2 = Label(Fr3, justify="left",text = '''A Cryptographic Algorithm Based on ASCII and Number System
     Conversions along with A Cyclic Mathematical Function
''',
                 fg="black",bg='white', font = "TimesNewRoman 18 bold",height=3).place(x = 220,y=10)
l1 = Label(Fr3, text = "Current System",fg="black",font = "TimesNewRoman 16 bold",bg='white',height=1,width=14).place(x = 450,y=120)


l3= Label(Fr3, text='''
In Existing system there are many cryptographic algorithms are introduced. 
One of the earliest and most used mechanisms in cryptography is Caesar's cipher 
which is also called a shift cipher.
It is a replacement mechanism in which each letter of the plain text is replaced by 
another letter which is certain places ahead of the letter and the process is repeated 
for all the letters in the plain text. 
The number of places ahead to be used is the key to the encryption. For example,
if the key is 2, then a will be replaced by c which is two places ahead of a.

''',
          fg="black",bg="white",justify=LEFT, font = "TimesNewRoman 12 bold",height=10).place(x = 250,y=180)

b8 = Button(Fr3, text = "Prev",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command = fr2).place(x = 50, y=500)
b7 = Button(Fr3, text = "Next",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command=fr4).place(x = 1050, y=500)

#--------------------Proposed System Page   ----Fr-4---------------------------------------------------------------------------------

ph5=ImageTk.PhotoImage(Image.open("bg5.jpg"))
lab4 = Label(Fr4,image=ph5).place(x = 0, y = 0)

lab2 = Label(Fr4, justify="left",text = '''A Cryptographic Algorithm Based on ASCII and Number System
     Conversions along with A Cyclic Mathematical Function
''',
                 fg="black",bg='white', font = "TimesNewRoman 18 bold",height=3).place(x = 220,y=10)
l1 = Label(Fr4, text = "Proposed System",fg="black",font = "TimesNewRoman 16 bold",bg='white',height=1,width=18).place(x = 450,y=120)


l3= Label(Fr4, text='''
Day by day the level of security is going to be higher. Still now many researchers are
working on cryptography and data hiding.A new cryptographic algorithm for the Real Time
Application was in to improve the time for encryption and decryption of data of end-to-end
delay and to provide higher level of security. In this paper, we proposed an improved
algorithmwhich is different from the traditional symmetric-key cryptography, asymmetric-key
cryptographyor hashing function.A cryptographic algorithm based on ASCII conversion and a cyclic
mathematicalfunction was presented in, and which makes the cipher differentfrom other algorithms.

 ''',
          
          fg="black",bg="white",justify=LEFT, font = "TimesNewRoman 12 bold",height=15,).place(x = 180,y=180)

b8 = Button(Fr4, text = "Prev",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command = fr3).place(x = 50, y=500)
b7 = Button(Fr4, text = "Next",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command=fr5).place(x = 1050, y=500)

#----------------Menu Page Fr-5 -------------------------------------------------------------------------

ph6=ImageTk.PhotoImage(Image.open("bg5.jpg"))
lab2 = Label(Fr5,image=ph6).place(x = 0, y = 0)

ll = Label(Fr5, text = "Menu",justify=LEFT,fg="black",bg="white",bd=5, font = "TimesNewRoman 14 bold",width=18,).place(x = 430, y =60)
b1 = Button(Fr5, text = "Home",justify=LEFT,fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fr1).place(x = 450, y =130)
b1 = Button(Fr5, text = "Abstract",justify=LEFT,fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fr2).place(x = 450, y =180)
b1 = Button(Fr5, text = "Current System",justify=LEFT,fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fr3).place(x = 450, y =230)
b1 = Button(Fr5, text = "Proposed System",justify=LEFT,fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fr4).place(x = 450, y =280)
b1 = Button(Fr5, text = "Encryption",justify=LEFT,fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fr6).place(x = 450, y =330)
b1 = Button(Fr5, text = "Decryption",justify=LEFT,fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fr9).place(x = 450, y =380)

b1 = Button(Fr5, text = "Close",justify=LEFT,fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=finish).place(x = 450, y =430)


#--------------------Encryption page-1   ----Fr-6---------------------------------------------------------------------------------

ph7=ImageTk.PhotoImage(Image.open("bg5.jpg"))
lab4 = Label(Fr6,image=ph7).place(x = 0, y = 0)
l22 = Label(Fr6, text = "ENCRYPTION",fg="black",font = "TimesNewRoman 20 bold",bg='white',height=1,width=11).place(x = 500,y=70)
l3= Label(Fr6, text = "Plain Text",fg="black",bg="white",bd=5, font = "TimesNewRoman 16 bold",height=1,width=14).place(x = 150, y =130)
e1=Entry(Fr6,bg="White",fg="black", font = "TimesNewRoman 16 bold",width=16)
e1.place(x = 400,y=130)

b1 = Button(Fr6, text = "Convert to ASCII",justify=LEFT,fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fun1).place(x = 150, y =180)
l3= Label(Fr6,textvariable= v1, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=42).place(x = 400,y=180)

l3= Label(Fr6, text = "Enter Key",fg="black",bg="white",bd=5, font = "TimesNewRoman 16 bold",height=1,width=12).place(x = 150, y =230)
e2=Entry(Fr6,bg="White",fg="black", font = "TimesNewRoman 16 bold",width=42)
e2.place(x = 400,y=230)

b1 = Button(Fr6, text = "Convert to ASCII",justify=LEFT,fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fun2).place(x = 150, y =280)
l3= Label(Fr6,textvariable= v2, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=42).place(x = 400,y=280)

b1 = Button(Fr6, text = "Product",fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fun3).place(x = 150, y =330)
l3= Label(Fr6,textvariable= v3, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=42).place(x = 400,y=330)

b1 = Button(Fr6, text = "Product Binary",fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fun4).place(x = 150, y =380)
l3= Label(Fr6,textvariable= v4, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=42).place(x = 400,y=380)
b8 = Button(Fr6, text = "Prev",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command = fr5).place(x = 50, y=500)
b8 = Button(Fr6, text = "Home",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command = fr1).place(x = 400, y=500)
b8 = Button(Fr6, text = "Clear",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command = clearE1).place(x = 500, y=500)
b7 = Button(Fr6, text = "Next",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command=fr7).place(x = 1050, y=500)


#--------------------Encryption page-2   ----Fr-7---------------------------------------------------------------------------------

ph8=ImageTk.PhotoImage(Image.open("bg5.jpg"))
lab4 = Label(Fr7,image=ph8).place(x = 0, y = 0)

b1 = Button(Fr7, text = "Matrix",fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fun5).place(x = 70, y =130)
b1 = Button(Fr7, text = "Transpose",fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fun6).place(x = 70, y =280)

b1 = Button(Fr7, text = "Convert to Values(CT1)",fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fun7).place(x = 70, y =450)
l3= Label(Fr7,textvariable= v25, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=42).place(x = 350,y=450)


b8 = Button(Fr7, text = "Prev",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command = fr6).place(x = 50, y=500)
b8 = Button(Fr7, text = "Home",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command = fr1).place(x = 400, y=500)
b8 = Button(Fr7, text = "Clear",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command = clearE2).place(x = 500, y=500)
b7 = Button(Fr7, text = "Next",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command=fr8).place(x = 1050, y=500)

#--------------------Encryption page-3   ----Fr-8---------------------------------------------------------------------------------

ph9=ImageTk.PhotoImage(Image.open("bg5.jpg"))
lab4 = Label(Fr8,image=ph9).place(x = 0, y = 0)

ph09=ImageTk.PhotoImage(Image.open("map1.jpg"))
lab4 = Label(Fr8,image=ph09).place(x = 700, y = 50)

l3= Button(Fr8, text = "Key Length KL",fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=14,command=fun8).place(x = 150, y =130)
l=Label(Fr8,textvariable= v26,bg="White",fg="black", font = "TimesNewRoman 16 bold",width=16).place(x = 400,y=130)

b1 = Button(Fr8, text = "CT1 + KL ",fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fun9).place(x = 150, y =200)
l3= Label(Fr8,textvariable= v27, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=42).place(x = 400,y=200)

b1 = Button(Fr8, text = "(CT1+KL) % 32",fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fun10).place(x = 150, y =250)
l3= Label(Fr8,textvariable= v28, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=42).place(x = 400,y=250)

b1 = Button(Fr8, text = "Cipher Text",fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fun11).place(x = 150, y =300)
l3= Label(Fr8,textvariable= v29, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=42).place(x = 400,y=300)

b8 = Button(Fr8, text = "Save Key",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",command = Savekeys).place(x = 450, y=500)
b8 = Button(Fr8, text = "Save CipherText",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",command = SaveCT).place(x = 280, y=500)

b8 = Button(Fr8, text = "Prev",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command = fr7).place(x = 50, y=500)
b8 = Button(Fr8, text = "Home",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command = fr1).place(x = 600, y=500)
b8 = Button(Fr8, text = "Clear",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command = clearE3).place(x = 700, y=500)
b7 = Button(Fr8, text = "Next",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command=fr9).place(x = 1050, y=500)


#--------------------Decryption page-1   ----Fr-9---------------------------------------------------------------------------------

ph10=ImageTk.PhotoImage(Image.open("bg5.jpg"))
lab4 = Label(Fr9,image=ph10).place(x = 0, y = 0)
l22 = Label(Fr9, text = "DECRYPTION",fg="black",font = "TimesNewRoman 20 bold",bg='white',height=1,width=11).place(x = 500,y=70)
b1 = Button(Fr9, text = "Browse Cipher Text",fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=OpenCode).place(x = 150, y =130)
l3= Label(Fr9,textvariable= v30, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=42).place(x = 400,y=130)

b1 = Button(Fr9, text = "Conver to ASCII",fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fun12).place(x = 150, y =180)
l3= Label(Fr9,textvariable= v31, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=42).place(x = 400,y=180)

b1 = Button(Fr9, text = "Browse Key",fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=OpenKey).place(x = 150, y =230)
l3= Label(Fr9,textvariable= v32, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=42).place(x = 400,y=230)

b1 = Button(Fr9, text = "Key Values",fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fun13).place(x = 150, y =270)
l3= Label(Fr9,textvariable= v33, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=42).place(x = 400,y=270)

b1 = Button(Fr9, text = "(A-k+32)%32",fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fun14).place(x = 150, y =320)
l3= Label(Fr9,textvariable= v34, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=42).place(x = 400,y=320)

b1 = Button(Fr9, text = "Binary",fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fun15).place(x = 150, y =370)
l3= Label(Fr9,textvariable= v35, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=42).place(x = 400,y=370)


b8 = Button(Fr9, text = "Prev",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command = fr8).place(x = 50, y=500)
b8 = Button(Fr9, text = "next ",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command=fr10).place(x = 1050, y=500)
b7 = Button(Fr9, text = "Clear",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command = clearD1).place(x = 560, y=500)



#--------------------Decryption Page-2   ----Fr-10---------------------------------------------------------------------------------

ph11=ImageTk.PhotoImage(Image.open("bg5.jpg"))
lab4 = Label(Fr10,image=ph11).place(x = 0, y = 0)

b1 = Button(Fr10, text = "4x4 matrix",fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=12,command=fun16).place(x = 100, y =130)
b1 = Button(Fr10, text = "Transpose of",fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=12,command=fun17).place(x = 100, y =250)

b1 = Button(Fr10, text = "Convert to Values",fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fun18).place(x = 100, y =400)
l3= Label(Fr10,textvariable= v36, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=42).place(x = 400,y=400)

b8 = Button(Fr10, text = "Prev",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command = fr9).place(x = 50, y=500)
b7 = Button(Fr10, text = "Clear",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command = clearD2).place(x = 560, y=500)
b7 = Button(Fr10, text = "Next",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command=fr11).place(x = 1050, y=500)



#--------------------Decryption Page-3   ----Fr-11---------------------------------------------------------------------------------

ph12=ImageTk.PhotoImage(Image.open("bg5.jpg"))
lab4 = Label(Fr11,image=ph12).place(x = 0, y = 0)

b1 = Button(Fr11, text = "Browse key 1",fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fun19).place(x = 150, y =130)
l3= Label(Fr11,textvariable= v37, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=42).place(x = 400,y=130)

b1 = Button(Fr11, text = "Convert to ASCII",fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fun20).place(x = 150, y =180)
l3= Label(Fr11,textvariable= v38, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=42).place(x = 400,y=180)

b1 = Button(Fr11, text = "Get Products",fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fun21).place(x = 150, y =230)
l3= Label(Fr11,textvariable= v39, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=42).place(x = 400,y=230)

b1 = Button(Fr11, text = "Divide with Key",fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fun22).place(x = 150, y =280)
l3= Label(Fr11,textvariable= v40, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=42).place(x = 400,y=280)

b1 = Button(Fr11, text = "Plain Text",fg="black",bg="white",bd=5, font = "TimesNewRoman 12 bold",height=1,width=18,command=fun23).place(x = 150, y =330)
l3= Label(Fr11,textvariable= v41, fg="black",bg="white",anchor="w", font = "TimesNewRoman 16 bold",width=42).place(x = 400,y=330)


b8 = Button(Fr11, text = "Prev",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command = fr10).place(x = 50, y=500)
b7 = Button(Fr11, text = "Clear",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command=clearD3).place(x = 560, y=500)
b7 = Button(Fr11, text = "Next",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command=fr12).place(x = 1050, y=500)


#===================CONCLUSION--Fr-12=======================================================
ph13=ImageTk.PhotoImage(Image.open("bg5.jpg"))
lab4 = Label(Fr12,image=ph13).place(x = 0, y = 0)

lab2 = Label(Fr12, justify="left",text = '''A Cryptographic Algorithm Based on ASCII and Number System
     Conversions along with A Cyclic Mathematical Function
''',
                 fg="black",bg='white', font = "TimesNewRoman 18 bold",height=3).place(x = 220,y=10)
l1 = Label(Fr12, text = "Conclusion",fg="black",font = "TimesNewRoman 16 bold",bg='white',height=1,width=10).place(x = 530,y=120)


l3= Label(Fr12, text='''
To ensure higher security and to hide data in effective way the proposed algorithm contributes greatly. Here, we

present an algorithm which is based on ASCII conversion and number system conversion and a cyclic mathematical

function. This algorithm not only encrypts the data but also hides the data which gives more security. In future

we will try to increase the security technique and implement some real time security system and try to add

Steganography with the system. 
''',
          
          fg="black",bg="white",justify=LEFT, font = "TimesNewRoman 12 bold",height=14).place(x = 150,y=180)

b8 = Button(Fr12, text = "Prev",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command = fr11).place(x = 50, y=500)
b7 = Button(Fr12, text = "Next",fg="black",bg="white",bd=5, font = "TimesNewRoman 10 bold",width=6,command=fr1).place(x = 960, y=500)



#==========================================================================
raise_frame(Fr1)
r.resizable(0,0)
r.geometry("1200x730+100+0")
r.title("A Cryptographic Algorithm Based on ASCII and Number System Conversions along with A Cyclic Mathematical Function")
r.mainloop()

