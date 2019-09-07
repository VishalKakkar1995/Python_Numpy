# Python_Numpy
Some basic programs I worked on using Numpy



#1: Write a program which will find all such numbers which are divisible by 7 

count=0
for i in range(2000,3201):
    if ((i%7==0) & (i%5!=0)):
        count+=1
        print (i)
print ("count = ",count)



#2. Write a program which can compute the factorial of a given numbers.   

print ('Enter a number for factorial')
a= int(input ())
b=1

print('The series is = ')
for i in range(a,0,-1):
    if (i!=a):
        print(" , ",(i))
    else:
        print(a)
    b=i*b
    
print('The factoial of input number is = ',(b))



#3. With a given integral number n, write a program to generate a dictionary that contains (i, i*i) such that is an integral number between 1 and n (both included). and then the program should print the dictionary.

print("Enter the number upto which you need the squared series")

a=int(input())
d={}
for i in range(1,a+1,1):
    a=i*i
    d[i]=a

print('The final result is',d)



#4. Write a program which accepts a sequence of "comma-separated" numbers from console and generate a list and a tuple which contains every number.

n=int(input(" Enter the number of elements you want in the list/tupple : ",))
L1=[]

for i in range(0,n,1):
    T1=int(input())
    
    L1.append(T1)
    
print("The list is",L1)

def convert(L1):
    return(tuple(L1))
           
print("The tuple is",convert(L1))



#6. Write a program that accepts a comma separated sequence of words as input and 


a=int(input("Enter the number of words you want =" ,))
L1=[]

for i in range (0,a,1):
    b=input("Enter the words ",)
    L1.append(b)
    
print("The Entered unsorted list is",L1)

L1.sort()

print("The sorted list is",L1)
    
    

#7. Write a program that accepts a sequence of whitespace separated words 


a=input("Enter the data : ")
t1=a.split()

t2=sorted(t1)
t3=unique(t2)


def unique(t2):
    
    return list(set(t2))


print(t1)
print(t2)
print(t3)



#8. Write a program that accepts a sentence and calculate the number of upper case 

a=input("Enter some data  ")

countu=0
countl=0

for i in a:
    if ((i.isupper())==1):
        countu=countu+1
    elif((i.islower())==1):
        countl=countl+1
        

print("The entered word was = ",a)
print("Number of lower charachters in the word = ",countl)
print("Number of upper charachters in the word = ",countu)



#9. A website requires the users to input username and password to register. Write a program to check the validity of password
#input by users. Following are the criteria for checking the password:
#1. At least 1 letter between [a-z]
#2. At least 1 number between [0-9]
#1. At least 1 letter between [A-Z]
#3. At least 1 character from [$#@]
#4. Minimum length of transaction password: 6
#5. Maximum length of transaction password: 12
#Your program should accept a sequence of comma separated passwords and will check them according to the above criteria. 
#Passwords that match the criteria are to be printed, each separated by a comma.

a=int(input("Enter the number of passwords you want =" ,))
L1=[]

for j in range (0,a,1):
    b=input("Enter the passwords ",)
    L1.append(b)


count1=0
count2=0
count3=0
count4=0
count5=0

for k in L1:
    for i in k:
        if((i.isupper())==1):
            count1=count1+1
        elif((i.islower())==1):
            count2=count2+1
        elif((i.isnumeric())==1):
            count3=count3+1
        elif((i=='$')|(i=='#')|(i=='@')):
            count4=count4+1
    if((len(k)>=6) &(len(k)<=12)):
        count5=count5+1 
        
    if((count1!=0)&(count2!=0)&(count3!=0)&(count4!=0)&(count5!=0)):
        print("Passed = ",k)
    else:
        print("Failed = ",k)
    count1=count2=count3=count4=count5=0
    
    
    
#10. Python has many built-in functions, and if you do not know how to use it, you can read document online or find some books.
#But Python has a built-in document function for every built-in functions.
#Please write a program to print some Python built-in functions documents, such as abs(), int(), raw_input()
#And add document for your own function
    
print("1. Abs funtion is for = ",abs.__doc__)
print("2. Int funtion is for = ",int.__doc__)
print("3. All funtion is for = ",all.__doc__)
print("4. Isinstance funtion is for = ",isinstance.__doc__)
print("5. Map funtion is for = ",map.__doc__)
    
