# **CH1 파이썬 문법**
## 자료형
#### 숫자형
정수 : 123, -20, 0\
실수 : 123, 45, -4321.5, 6, 6.08e9  
8진수 : 0o456, 0o123  
16진수 : 0xFF, 0X00, 0X0A  
####  변수
* 문자 또는 밑줄로 시작(beta,_kim)
* 대소문자를 구분(sum, Sum, SUM)
* 영문자,숫자,밑줄(A-z,0-9,_)
* 파이썬 키워드는 사용 불가.
~~~    
    a = 10  
    b = 20 
    c = a + b  
    d = b - a
    print(c, d)
~~~
~~~
a = 10
b = 3
 #나눗셈
c = a/b  #  나눗셈  
d = a//b  #  몫  
e = a%b  #  나머지 
 # 곱셈
f = a*b 
g = a**b #제곱
print(c,d,e,f,g) 
~~~
#### 문자열
1. 큰 따옴표 "Hello World"  
2. 작은 따옴표 : '대한민국'  
3. 큰 따옴표 3개 : """Hello!"""
4. 작은 따옴표 3 : 
'''Life is too short. You need 
python '''  
~~~
myName = "Sebin Oh" #낙타표기법 (중간 대문자)
my_Name = "오세빈" #스네이크 표기법 (_언더바 사용한 것)
MyName = 'kiki' # 파스칼 표기법 (앞 대문자)
_my_name = "korea"
MYNAME = "God is love"
my2name = "12345"
# 2myname = '9876' 숫자로 시작할 수 없다.
# my-name = "michle" 위에바가 들어가면 안된다.
# my name = "kiki" 스페이스바를 쓰면 안된다.
myStr = '123' #str
myNum = 123 # int

print(myStr, myNum)
#print(myStr+myNum) 숫자와 문자이기 때문에 합해지지않는다.
print(type(myStr))
print(type(myNum))
~~~
##**여러개 변수 할당**
~~~
x,y,z = "포도", "딸기", "수박"
print(x)
print(y)
print(z)
~~~
~~~
 a = b = c = "오렌지"
 print(a)
 print(b)
 print(c)
~~~
~~~
fruits = ["포도", "딸기", "수박"]
x , y , z = fruits
print(x)
print(y)
print(z)
~~~
~~~
x = "Life"  
y = "is"  
z = "Beautiful"  
print(x,y,z)
print(x+y+z)
~~~
~~~
a = 1
b = 2
c = 3 # "3" str 으로 만들면 에러가 난다.
print(a,b,c)
print(a+b+c)
~~~
### **데이터 유형**
+ 텍스트
+ 숫자
+ 불(bool)
~~~
a = 100
b = 200
result = a + b
print(a,  '+'  ,  b,  '='  , result)  
result = a - b
print(a,  '-'  ,  b,  '='  , result)  
result = a * b
print(a,  '*'  ,  b,  '='  , result)  
result = a / b
print(a,  '/'  ,  b,  '='  , result)  
~~~
#### input() 함수 이용한 계산기  
~~~
a = int(input("첫번째 숫자를 입력해 주세요: "))
b = int(input("두번째 숫자를 입력해 주세요: "))
result = a + b
print(a, "+", b, "=" , result)
result = a - b
print(a, "-", b, "=" , result)
result = a * b
print(a, "*", b, "=" , result)
result = a / b
print(a, "/", b, "=" , result)
# input 사용 사칙연산 계산기
~~~
~~~
a = int(input("첫번째 숫자를 입력해 주세요: "))
b = int(input("두번째 숫자를 입력해 주세요: "))
result = a ** b
print(a, "**", b, "=" , result)
result = a // b
print(a, "//", b, "=" , result)
result = a % b
print(a, "%", b, "=" , result)
# input 사용 제곱 몫 나머지 계산기
~~~
