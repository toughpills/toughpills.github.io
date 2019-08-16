# toughpills.github.io
## python study daily 0815


if 
number = 23
guess = int(input("enter an integer: "))

if guess ==number:
    print("congratulations, you have guessed it,"\
          "but you cannot win any prizes.")
elif guess < number:
    print("sorry, it's a little higher than that,"\
          "you can try again")
else:
   print("no, it is smaller than that,"\
          "please try another time")
print("DONE")

    
####while
number = 23
running = True   ######a loop

while running:
    guess = int(input("enter an integer: "))
    if guess == number:
        print("congratulations, you guessed it.")
        running = False   #### a loop tp stop here
    elif guess != number:
        print('please try again')
else:
    print("the loop is over.")
print("DONE")


####while + break
while True:
    s = input("enter a word ")
    if s == "quit":
        break
    print("the length of the word is ", len(s))

####while + continue
while True:
    s = input("enter")
    if s == "quit":
        break
    if len(s)<3:
        continue
    print("input is off sufficient")

####for
for i in range(1,5):
    print(i+1)
else:
    print(i)

####def function
def printMax(a,b):
    if a>b:
        print(a,"is maximum")
    else:
        print(b,"is maximum")

##printMax(8,9) #调用的形式之一
x = 8
y = 9
printMax(x,y) ##调用的形式之二

####def 局部变量
def function(x):
    print("x is ", x)
    x = 2
    print('changed local x to', x)

x = 3
function(x)
print("x is still ", x)

####global语句可以为定义在函数外的变量赋值
def func():
    global x
    print("x is ", x)
    x = 2
    print("changed local x to",x)
x = 3
func()
print("x is now",x)

####参数默认数值，要先声明没有默认值的参数，再声明有默认值的参数
def say(meassage, times=1):
    print(meassage*times)
say("Chicken is not my style",5)


####使用关键参数，使用关键词而非位置来给函数指定实参
def fun(a, b = 2, c = 3):
    print("a is", a,\
          "b is",b,\
          "c is",c)
fun(1,4)
fun(1, c = 4)


######return 从一个函数返回或从函数返回一个值,没有return返回值的语句等价于return none。
def maxmium(x,y,z):
    return(max(x,y,z))    
print(maxmium(2,3,4))

######DocStrings：文档字符串'''    '''  help(printMax)抓取函数的属性，然后展示出来，q退出help
def printMax(x,y):
##        The two values must be integers.'''
   x = int(x)
   y = int(y)
    if x > y:
        print(x,"is maximum")
    else:
        print(y,"is maximum")
printMax(77,88.2)

######sys模块--system
import sys
print("the command line arguments are: ")
for i in sys.argv:
    print(i)
print("\n\nThePYTHONPATH is",sys.path,"\n")
