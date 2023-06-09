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
~~~
#잘못된 예시 
num1 = input("숫자입력1:  ")
num2 = input("숫자입력2:  ")
result = num1 + num2
print(type(num1))
print(num1, "+", num2, "=", result)
# 이렇게하면 num이 스트링으로 잡히기 때문에 int를 넣어줘야한다.
~~~
~~~
a = input("이름을 입력해주세요: ")
b = input("전화번호를 입력해주세요: ")
c = int(input("무게를 입력해주세요 (g단위) "))
result = c*10
print("이름은", a, "전화번호는",  b , "무게에 따른 금액은", result  ,"입니다")
~~~
### **2.print() 서식 출력**  
print("%d" % 123)//정수 표시  
print("%5d" % 123)//정수 0 제외 5자리 표시  
print("%05d" % 123)//정수 0 포함 5자리 표시  
~~~
print("%d" % 123)
print("%5d" % 123)  
print("%05d" % 123)
~~~
print("%f" % 123.45)//소수표시  
print("%7.1f" % 123.45)//소수 표시 7자리 확보 후 첫재자리까지 표시  
print("%7.3f" % 123.45)//소수 표시 7자리 확보 후 셋째자리까지 표시  
~~~
print("%f" % 123.45)
print("%7.1f" % 123.45)  
print("%7.3f" % 123.45)
~~~
print("%s" % "대한민국")//문자 표시  
print("%6s" % "대한민국")//문자 6자리로 표시  
~~~
print("%s" % "대한민국")
print("%6s" % "대한민국")
~~~
### **Format 함수: 순거 지정 가능**  
~~~
print("{0:d} {1:5d} {2:05d}".format(123,456,789))
~~~
~~~
print("{2:d} {1:5d} {0:05d}".format(123,456,789))
~~~

위 두 예문 중 0과 2의 순서를 바꾸어주었더니  
123(0)이 789(2)와 순서가 바뀜을 볼 수 있었다.  
## **서식 출력**  
~~~
print("\n줄바꿈\n연습입니다.")
~~~
~~~
print("\t탭키\t연습.")
~~~
~~~
print("글자가 \"강조\"되는 효과1")  
print("글자가 \'강조\'되는 효과2")  
print("역슬레시 3개출력 \\\\\\")
print(r"\n \t \" \\ \' @를 그대로 출력")
~~~
### **관계 연산자**  
~~~
a,b = 10, 20  
print(a==b, a!=b, a>b, a<b, a>=b, a<=b)
~~~
### **논리 연산자**  
~~~
a = 99
print((a>100) and (a<200))
print((a>100) or (a<200))
print(not (a==100))
~~~
~~~
if(123):  
  print("참이면 보입니다.")
if(0):  
  print("거짓이면 보입니다")
~~~
### 퀴즈2 숫자 입력을 받아 동전으로  바꿔주는 프로그램( 500원, 100원, 50원, 10원) 나머지는 거스름 돈으로 출력  
1.내가 만든예제
~~~
bill = int(input("총액을 입력해주세요"))

rest500=bill%500
c500=bill//500

rest100=rest500%100
c100=rest500//100

rest50 = rest100%50
c50 = rest100//50

rest10 = rest50%10
c10 = rest50//10

final=rest10

print("총액", bill, "500원은", c500,"100원은", c100,"50원은", c50,"10원은", c10, "거스름돈은", final  ,"입니다")
~~~
교수님이 만든 예제
~~~
bill,c500, c100, c50, c10 = 0,0,0,0,0
bill = int(input("바꿀돈은?"))

c500 = bill // 500 #몫
bill %=500 # bill =bill%500
c100 = bill // 100 #몫
bill %=100 # bill =bill%100
c50 = bill // 50 #몫
bill %=50 # bill =bill%50
c10 = bill // 10 #몫
bill %=10 # bill =bill%10

print("500원짜리 %d개" % c500)
print("100원짜리 %d개" % c100)
print("50원짜리 %d개" % c50)
print("10원짜리 %d개" % c10)
print("잔돈 %d원" % bill)
~~~
### **조건문**  
~~~
a=150
if(a<100):
  print("100보다 작음")
else :  
  print("100보다 크다")
  print("프로그램 끝")
~~~
~~~
a = int(input("정수를 입력하세요 : "))
if( a % 2 == 0):
  print("짝수")
else :  
  print("홀수")
~~~
~~~
a = 120
if(a>50):
  if(a<100):
    print("50<a<100")
  else:
    print("a>100")
else:
  print("a<50")
~~~
~~~
fruit=['사과','배','감','포도']
fruit.append("딸기")
if '딸기' in fruit :
  print("딸기가 있습니다")
print(fruit)
~~~
~~~
import random

number = []
for num in range(0,7) : 
  number. append(random.randrange(1,46))
print("생성된 리스트", number)
~~~
### **반복문**  
~~~
for i in range(0,3,1): #시작값,끝값+1,증가값
  print("%d 안녕하세요~" % i) #반복 내용
  #print(i)
print("반갑습니다")
~~~
~~~
for i in range(1,9,1):
  print("%d " % i, end="")  
print("\n")
for i in range(1,9,1):
  print("\n%d" % i, end=" ")
~~~
~~~
sum=0
for i in range(1,11,1):
  sum = sum+ i
print("1~10까지 합계 : %d" % sum)
~~~
### **QUIZ3** : 숫자 입력을 받아 1부터 입력된 숫자까지의 합을 for문을 활용하여 출력하시오  
~~~
sum,num=0,0
num = int(input("숫자입력 : "))
for i in range(1,num+1,1):
  sum = sum+ i
print("1~n까지 합계 : %d" % sum)
~~~
### **중첩 for문**  
~~~
i,j,k=0,0,0
k= int(input("구구단 단수 입력 : "))
for i in range(1,10,1):
    print("%d x %d = %2d" % (k,i,k*i))
print("")
~~~
### **quiz 구구단을 2,3,4,5 출력 후 줄바꿔서 출력하시오**  
~~~
m,n=0,0
for m in range(1,10,1):
  for n in range(2,6,1):
      print("%d x %d = %2d" % (n,m,m*n), end='\t')     
  print("")
print("\n")
m,n=0,0
for m in range(1,10,1):
  for n in range(6,10,1):
   print("%d x %d = %2d" % (n,m,n*m), end='\t' )
  print("") 
~~~
# CH3. 자료형  

## 1. 인덱스와 슬라이싱  
  
  
~~~
L = [0,1,2,3,4,5,6,7,8,9]
print(L[1])
~~~
~~~
L = [0,1,2,3,4,5,6,7,8,9]
print(L[-3])
~~~
~~~
L = [0,1,2,3,4,5,6,7,8,9]
print(L[0:9])
~~~
~~~
L = [0,1,2,3,4,5,6,7,8,9]
print(L[0:9:2])
~~~
~~~
L = [0,1,2,3,4,5,6,7,8,9]
print(len(L))
print(L[len(L)-1])
~~~
~~~
L = [0,1,2,3,4,5,6,7,8,9]
L[0] = 99
L[9] = '가나다'
L[1] = [1,2,3]
print(L)
print(L[9])
~~~
~~~
a = [1,2,3]
b = [4,5,6]
c = a+b
print(a+b)
print(c)
print(a*3)
~~~
~~~
L = [1,2,3,4,5]
print(L)
L.append(6) #리스트 뒤에 추가
print(L)
L.remove(3) #해당 요소값을 삭제
print(L)
~~~
~~~
k=['a', 'b', 'c', 'd']
k.remove('d')
print(k)
~~~
~~~
k='God is love!'
print(k[:3])
print(k[6:])
print(k[-8:-1])
~~~
L = [0,1,2,3,4,5,6,7,8,9]  
a = [1,2,3]  
b = [4,5,6]  
d=['a', 'b', 'c', 'd']
e='God is love!'  
[3] 일경우 3 (0부터 3 즉 4번째 배열숫자)  
[-3] 일경우 7 (0부터 -3 즉 -3번째 배열숫자)  
[0:3] 일경우 0 1 2 (0부터 2(3-1)까지)  
[0:5:2] 일경우 0 2 4 (0부터 4(5-1)까지 2의 배수)  
print(len(L)) 일 경우 10 (배열된 숫자 갯수)  
print(L[len(L)-1]) 일 경우 9  (배열된 숫자 갯수 -1)  
L[0] = 99 (배열된 숫자 0 번째를 99로 바꿈)  
L[9] = '가나다' (배열된 숫자 9 번째를 문자 가나다 로 바꿈)  
L[1] = [1,2,3] (배열된 숫자 1 번째를 [1,2,3]으로 바꿈)  
c = a+b (a와b를 더함)  
print(a*3) (a를 3번 출력)  
L.append(10) (리스트 뒤에 추가)  
L.remove(3) (해당 요소값을 삭제)  
d.remove('d') (d라는 문자 삭제)  
print(e[:3]) (God 즉 0~2 문자 출력)  
print(e[6:]) (love! 즉 6번째 부터 끝까지 출력)  
print(e[-8:-2]) (-8번째부터 -2번째 까지 출력)  
~~~
k= ' God is love! '
print(k.upper())
print(k.lower())
print(k.strip())
~~~
~~~
a = ' God, is, love! '
print(a.split(","))
~~~
~~~
a = ['apple', 'banana', 'cherry']
a.append('orange')
print(a)
~~~
~~~a = ['apple', 'banana', 'cherry']
a.insert(1,'orange') #지정한 곳에 삽입
print(a)
~~~
~~~
a = ['apple', 'banana', 'cherry']
a.remove('banana')
print(a)
~~~
~~~
a = ['apple', 'banana', 'cherry']
a.pop() # index가 없으면 맨뒤를 지움(cherry지움)
print(a)
a.pop(1) # 0포함 1 번째 즉 banana 지움(지정된 위치 삭제)
print(a)
~~~
~~~
a = ['apple', 'banana', 'cherry']
del a[0]
print(a)
a.clear()  #del a
print(a)
~~~
~~~
#fruit 에 있는 내용만큼 표시
fruit = ['apple', 'banana', 'cherry']
for x in fruit:
  print(x)
~~~
~~~
#fruit 에 있는 내용만큼 전체 내용 표시
fruit = ['apple', 'banana', 'cherry']
for i in range(len(fruit)):
  print(fruit)
~~~
### **SORT**
~~~
a = [5,3,6,8,1,9,0]
a.sort()
print(a)
~~~
~~~
a = [5,3,6,8,1,9,0,2,4,7]
a.sort(reverse = True) # 거꾸로
print(a)
a.sort() # 정방향
print(a) 
~~~
~~~
fruit = ['banana','apple', 'Kiwi', 'cherry','Orange']
fruit.sort() #대소문자 구분하여 정렬
print(fruit)
fruit.sort(key=str.lower) #대소문자 구분 없이 정렬
print(fruit)
fruit.reverse()
print(fruit)
~~~
~~~
# list 복사
fruit = ['banana','apple', 'Kiwi', 'cherry','Orange']
myList = fruit.copy()
print(myList)
cpList = list(fruit)
print(cpList)
~~~
### **2.Tuple**  
~~~
l= [1,2,3]
t = (4,5,6)
l[0] = 5
print(l)
# t[0] = 1  
# ()는 불가능
print(t)
~~~
~~~
f = ['banana','apple', 'Kiwi', 'cherry','Orange']
print(len(f))
~~~
~~~
t = ('apple',)
print(t)
print(type(t))
f = ('banana') #튜플로 인식하기 위해서는 ","필요
print(f)
print(type(f))
~~~
~~~
f = ('banana','apple', 'Kiwi', 'cherry','Orange')
print(f[:4])
print(f[2:])
~~~
~~~
f = ('banana','apple', 'Kiwi', 'cherry','Orange')
if 'apple' in f :
  print("Yes, 'apple' is in")
else:
    print('No')
~~~
### **list<-->tuple**
~~~
firm = ['Samsung','LG','SK']
tdata = tuple(firm)
print(firm)
print(tdata)
~~~
~~~
# tuple에 추가
t = ('banana','apple', 'Kiwi', 'cherry')
y = list(t)
y.append('Orange')
t = tuple(y)
print(t)
~~~
~~~
#tuple과 tuple 끼리는 더해진다
t = ('apple', 'banana', 'cherry')
q = ('kiwi',)
t += q 
print(t)
~~~
~~~
t = ('apple', 'banana', 'cherry', 'kiwi')
l = list(t)
l.remove('apple')
t = tuple(l)
print(t)
del t
# print(t) 삭제가능하지만 삭제후 출력불가
~~~
### **3.dict 사전자료형**
~~~
d = {
    'a':1,
    'b':2,
    'c':3
}
print(d)
print(d.keys())
print(d.values())
print(d.items())
~~~
~~~
car={
    'brand' : 'BMW',
    'model' : 'GT',
    'year' : 1988
}
print(car)
print(len(car))
car["year"] = 2000 
car["item"] = 123456
car.update({"color" : "red"})
print(car)
~~~
~~~
#항목 제거
car={
    'brand' : 'BMW',
    'model' : 'GT',
    'year' : 1988
}
car.pop('model')
print(car)
~~~
~~~
car={
    'brand' : 'BMW',
    'model' : 'GT',
    'year' : 1988
}
car.popitem()
print(car)
~~~
~~~
car={
    'brand' : 'BMW',
    'model' : 'GT',
    'year' : 1988
}
car.clear() # 비움
del car #삭제
~~~
### **LOOP**
~~~
#값
car={
    'brand' : 'BMW',
    'model' : 'GT',
    'year' : 1988
}
for x in car :
  print(car[x])
~~~
~~~
car={
    'brand' : 'BMW',
    'model' : 'GT',
    'year' : 1988
}
for x in car.values() :
  print(x)
~~~
~~~
car={
    'brand' : 'BMW',
    'model' : 'GT',
    'year' : 1988
}
for x in car.keys() :
  print(x)
~~~
~~~
car={
    'brand' : 'BMW',
    'model' : 'GT',
    'year' : 1988
}
for x,y in car.items() :
  print(x,y)
~~~
~~~
car={
    'brand' : 'BMW',
    'model' : 'GT',
    'year' : 1988
}
myCar = car.copy()
print(myCar)
~~~
~~~
car={
    'brand' : 'BMW',
    'model' : 'GT',
    'year' : 1988
}
myCar = dict(car)
print(myCar)
~~~
~~~
name1 = {"name" : "홍길동", "year":2001}
name2 = {"name" : "갑돌이", "year":2010}
name3 = {"name" : "감순이", "year":2003}
family = {
    "name1" :name1,
    "name2" :name2,
    "name3" :name3
}
print(family)
~~~
## **CH4 조건문,반복문**  
### **중첩 IF문**  
~~~
score = int(input("점수를 입력해주세요 : "))
if (score > 100):
  print("0~100까지의 숫자로 입력하세요")
elif(score >=90):
  print("점수:%3d A"%score)
elif(score >= 80):
  print("점수:%3d B"%score)
elif(score >=70):
  print("점수:%3d C"%score)
elif(score >=60):
  print("점수:%3d D"%score)
else:
  print("점수:%3d F"% score)
print("학점 입니다.")
~~~
~~~
import random

numbers = []
for num in range(0,10):
  numbers.append(random.randrange(0,10))

print("생성된 리스트", numbers)

for num in range(0,10):
  if num not in numbers:
    print("숫자 %d는 리스트에 없습니다" %num)
  else:
    print("숫자 %d는 리스트에 있습니다" %num)
~~~
~~~
select, answer, numStr, num1, num2 = 0,0,"",0,0

select = int(input("1.입력한 수식 계산 2.두수의 합계: "))

if select == 1:
  numStr = input("*** 수식을 입력하세요 : ")
  answer = eval(numStr) # 1+2. "string"+"str"
  print(" %s 결과는 %5.1f입니다. " %(numStr,answer))
elif select == 2:
  num1 = int(input("*** 첫번째 숫자를 입력하세요 : "))
  num2 = int(input("*** 두번째 숫자를 입력하세요 : "))
  for i in range(num1,num2+1):
    answer = answer + i
  print("%d+...+%d는 %d입니다  " %(num1,num2,answer))
else:
  print("1또는 2만 입력해야 합니다.")
~~~
### **for & while 반복문**  
~~~
for i in range(0,3,1):
  print("안녕!")
~~~
~~~
for i in [0,3,1]:
  print("안녕@")
~~~
~~~
for i in range(1,3,1):
  for j in range(1,2,1):
    print("i:%d, j:%d" %(i,j))
~~~
~~~
i,j = 0,0
for i in range(1,10,1):
  for j in range(2,10,1):
    print("%d x %d = %2d" %(j,i,i*j), end='\t')
  print("")
print("\n")
~~~
~~~
i = 0
while i<3:
  print("%d : while문" %i)
  i = i+1
~~~
~~~
# Q 1부터 10까지 합계를 while, for문으로
i, hap = 0,0
i = 1
while i<11:
  hap = hap + i
  i=1+i

print("1부터 10까지의 합계: %d" %hap)
~~~
~~~
# Q 1부터 10까지 합계를 while, for문으로
i, hap = 0,0
for i in range(1,11,1):
  hap = hap+i

print("1부터 10까지의 합계: %d" %hap)
~~~
~~~
#while True:
print("무한 루프ㅠㅠ", end='')
~~~
~~~
#break
for i in range(1,100):
  print("for문 %d번 실행" %i)
  break # 브레이크는 루프 안에서 빠지게 해준다
print("break 빠짐")
~~~
~~~
hap = 0
a,b = 0,0
while True:
  a = int(input("덧셈 첫번째 수 입력: "))
  if a==0:
    break
  b = int(input("덧셈 두번째 수 입력: "))
  hap = a + b
  print("%d + %d = %d" %(a,b,hap))

print("break로 탈출")
~~~
~~~
# continue
hap, i = 0,0
for i in range(1,11):
  if i % 3 == 0:
    print("i:%d" %i)
    continue
  hap += i

print("1~10 합계(3의 배수 제외): %d" %hap)
~~~
~~~
fruits = ["사과","바나나","체리"]
for x in fruits:
  if x == "바나나":
    continue
  print(x)
~~~
~~~
for x in range(6):
  print(x)
else:
  print("끝")
~~~
~~~
for x in range(6):
  if x ==3: break
  print(x)
else:
  print("끝")
~~~
~~~
# for  문 루프는 비워 둘수 없음
for x in [0,1,2]:
  pass
~~~
## **함수**  
~~~
# 두수를 더하는 함수
def plus(v1,v2):
  result = 0 #초기화
  result = v1 + v2
  return result

hap = 0
hap = plus(10,20)
print("10+20 plus() 처리 결과는 %d" %hap)
hap = plus(20,30)
print("10+20 plus() 처리 결과는 %d" %hap)
~~~
### **계산기 코드**  
~~~
# 계산기 코드
def calc(v1,v2,op):
  result = 0
  if op == '+':
    result = v1 + v2
  elif op == '-':
    result = v1 - v2
  elif op == '*':
    result = v1 * v2
  elif op == '/':
    result = v1 / v2
  return result

rst = 0
var1 , var2, opr = 0,0,""

opr = input("(+,-,*,/) 입력")
var1 = int(input("1번째 수 입력: "))
var2 = int(input("2번째 수 입력: "))
rst = calc(var1,var2,opr)

print("계산기 %d %s %d = %d" %(var1, opr, var2, rst))
~~~
### **Q 0으로 나누려고 하면 계산되지 않게 메세지 출력,**   
### **제곱 연산자 추가(숫자1, 연산자, 숫자2) 계산기 함수 만들기**  
~~~
def calc(a, b, k):
result = 0
if k == '+':
result = a + b
elif k == '-':
result = a - b
elif k == '*':
result = a * b
elif k == '/':
if b!=0:
result = a / b
elif k == '**':
result = a ** b
return result


while True:
a = int(input("첫 번째 숫자를 입력하세요: "))
k = input("연산자를 입력하세요 (+, -, *, /, ** 중 택 1): ")
b = int(input("두 번째 숫자를 입력하세요: "))
res = calc(a, b, k)
if b==0 and k=="/":
print("0으로 나눌 수 없습니다.")
break
else:
print("계산기 : %d %s %d = %d" % (a, k, b, res))
continue
continue_calculation = input("계속 계산하시겠습니까? (Y/N): ")
if continue_calculation.upper() == 'N':
break
elif continue_calculation.upper() == 'Y':
continue
~~~
~~~
# 전역 변수와 지역변수
def func1():
  a = 10 # 지역변수
  print("func1()에서 a값 %d" %a)

def func2():
  print("func2()에서 a값 %d" %a)

a= 20 # 지역변수

func1()
func2() #함수내 선언이 먼저
~~~
## **Ch5 파일 처리**  
"r" read  
"a" append  
"w" write  
"x" create  
"t' text  
"b" binary  
~~~
# w
from google.colab import files

f = open("a.txt","w")
f.write("12345")
f.close()

f = open("a.txt","w")
f.write("abcde")
f.close()

files.download('a.txt')
~~~
~~~
from google.colab import files

f = open("a.txt","w")
f.write("12345")
f.close()

f = open("a.txt","a")
f.write("6789")
f.close()

files.download('a.txt')
~~~
~~~
from google.colab import files
#생성된 파일이 있으면 에러
f = open("b.txt","x")
f.write("abcde")
f.close()

files.download('b.txt')
~~~
~~~
# 여러줄 내용 입력

from google.colab import files
f = open("a.txt","w")
#f.write("12345678\n987654321\nabcde")
f.write("""1234
5678
890""")
f.close()

files.download('a.txt')
~~~
~~~
#리스트, 튜플 내용을 입력
from google.colab import files

t = ("1","2","3","4","\n")
l = ["a","b","c","d"]
f= open("a.txt",'w')
for i in range(0,5):
  f.writelines(t[i])
#f.writelines(t)
f.writelines(l)
f.close()

files.download('a.txt')
~~~
~~~
# read 모드로 파일 열기
from google.colab import files

f = open("a.txt","w")
f.write("1234\n567")
f.close()

f = open("a.txt","r")
print(f.read())
f.close()


files.download('a.txt')
~~~
~~~
# readlines() 함수 : 한줄씩 가져옴
from google.colab import files

f = open("a.txt","r")
print(f.readline())
print(f.readline())
f.close()

files.download('a.txt')
~~~
~~~
from google.colab import files
#파일 삭제
import os
if os.path.exists("a.txt"):
  os.remove("a.txt") #os.rmdir("folder")
else:
  print("파일이 없음")
~~~
~~~
from google.colab import files
import os

print(os.listdir('.'))
os.rename("b.txt","a.txt") #file 이름 변경
print(os.listdir('.'))
~~~
~~~
from google.colab import files
import os
# file 존재 유무 확인
print(os.path.exists('a.txt'))
print(os.path.exists('b.txt'))
~~~
~~~
#구구단 파일로 저장
from google.colab import files
import sys

f = open("a.txt","w",encoding ='utf8')
sys.stdout = f 
for i in range(2,10):
  for j in range(1,10):
    print("{} x {} = {}".format(i,j,i*j))
print()
f.close()

files.download('a.txt')
~~~
# **VISUAL STUDIO CODE**  
~~~
def Hello():
    "함수의 설명을 적을수 있음"
    print("안녕하세요~")
    print("파이썬 함수 연습입니다.")

Hello()
help(Hello)
~~~
~~~
c=0
def add(a,b):
    "두개의 변수를 받아 더하는 함수"
    global c 
    c= a+b
    print(c)#pass

def addr(a,b):
    return a+b

add(10,20)
print(c)
print("--------------------")
y = addr(10,20)
print(y)
~~~
~~~
a = 20 #전역변수
def func():
    a = 10 #지역변수
    print(a)

func()
print(a)
~~~
~~~
def func():
    b = 10 #지역변수
    print(b)

func()
print(b) #error
~~~
~~~
a=10
def func():
    b = 20
    return a + b
x = func()
print(x)
~~~
~~~
def func(a,b=20): #20이 앞에오면 에러 
    print(a+b)

func(10,30)
~~~
~~~
from tkinter import *

window = Tk()

#
window.title("윈도우 창 연습")
window.geometry("400x400") # x는 소문자로
window.resizable(width=True, height=FALSE)

window.mainloop()
~~~
~~~
from tkinter import *

window = Tk()

window.title("레이블")
label1 = Label(window, text="안녕하세요! 오세빈 입니다.")
label2 = Label(window, text="Python<br>Korea", font=("궁서체",30), fg="red")
label3 = Label(window, text="Love is", bg="yellow",width=20, height=5, anchor=E)

label1.pack()
label2.pack()
label3.pack()

window.mainloop()
~~~
~~~
from tkinter import *

window = Tk()



help(Tk())
window.mainloop()
~~~
~~~
from tkinter import *

window = Tk()

window.title("김일과 이노키")
photo=PhotoImage(file = "C:\\Users\\user\\Pictures\\kdg.png")
photo2=PhotoImage(file = "C:\\Users\\user\\Pictures\\ZZZ.png")
label1 = Label(window, image = photo)
label2 = Label(window, image = photo2)

label1.pack(side=LEFT)
label2.pack(side=RIGHT)
window.mainloop()
~~~
~~~
from tkinter import *

tk = Tk()
tk.geometry("400x400")
button1 = Button(tk, text="파이썬 종료", fg="blue", bg="yellow", command=quit)
button1.pack()




tk.mainloop()
~~~
~~~
from tkinter import *
from tkinter import messagebox

def myFunc():
    messagebox.showinfo("박치기 버튼", "잡박 너무 멋있죠^^")


tk = Tk()
photo = PhotoImage(file="C:\\Users\\user\\Pictures\\kdg.png")
button1 = Button(tk, image=photo, command=myFunc)

button1.pack()
tk.mainloop()
~~~
## html Visual studio Code 이용 
~~~
<!DOCTYPE html>
<html>
    <head>HTML Basic</head>
    <body>
        <h1>헤딩 1</h1>
        <h2>헤딩 2</h2>
        <h3>헤딩 3</h3>
        <h4>헤딩 4</h4>
        <h5>헤딩 5</h5>
        <h6>헤딩 6</h6>
        <p>선언 !DOCTYPE은 문서 유형을 나타내며 브라우저가 <br/>웹 페이지를 올바르게 표시하도록 도와줍니다. 페이지 상단</p>
    </body>
</html>
~~~
~~~
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Site Link</title>
</head>
<body>
    <h1>사이트 링크</h1>
    <a href="http://www.naver.com">네이버</a><br>
    <a href="http://www.google.com">구글</a>
    <p><i>안녕하세요</i>저는<b>잡박</b>입니다</p>
</body>
</html>
~~~
~~~
        <!DOCTYPE html>
        <html lang="ko">
        <head>
            <meta charset="UTF-8">
            <meta http-equiv="X-UA-Compatible" content="IE=edge">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <title>HTML Image</title>
        </head>
        <body>
            <h1>브라우저 열기 alt+B</h1>
            <p>가나다라</p>
            <h1>image</h1>
            <img src="C:\Users\user\Pictures\kdg.png" width="200" height="200">
        </body>
        </html>
~~~
~~~
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Style</title>
</head>
<body>
    <h1 style="color: red;">This is red color</h1>
    <h1 style="color: blue;">This is blue color</h1>
    <p style="background-color: yellow;">CSS color속성은 HTML 요소의 텍스트 색상을 정의합니다.</p>
    <p style="font-size: 200%; font-family:'Courier New', Courier, monospace;">문장을 나타내는 p태그</p>
</body>
</html>
~~~
~~~
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RGB Color</title>
</head>
<body>
    <h1 style="background-color: rgb(255,0,0,0.2);">rgb(255,0,0,0.2)</h1>
    <h1 style="background-color: rgb(255, 255, 0);">rgb(255,255,0)</h1>
    <h1 style="background-color: rgb(0, 255, 0);">rgb(0,255,0)</h1>
    <h1 style="background-color: rgb(0, 255, 255);">rgb(0,255,255)</h1>
    <h1 style="background-color: rgb(0, 0, 255);">rgb(0,0,255)</h1>
    <h1 style="background-color: rgb(255, 255, 255);">rgb(255,255,255)</h1>
    <h1 style="background-color: rgb(0, 0, 0,0.2);">rgb(0,0,0,0.2)</h1>
    <h1 style="background-color: #ee82ee">#ee82ee</h1>
</body>
</html>
~~~
~~~
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>순서없는 리스트</title>
</head>
<body>
    <h2>좋아하는 과일</h2>
    <ul type="Circle">
        <li>사과</li>
        <li>바나나</li>
        <li>딸기</li>
        <li>감</li>
    </ul>
</body>
</html>
~~~
~~~
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>순서있는 리스트 ol</title>
</head>
<body>
    <h2>좋아하는 가수</h2>
    <ol type="A"> #i, 1
        <li>블랙핑크</li>
        <li>아이브</li>
        <li>방탄소년단</li>
    </ol>
</body>
</html>
~~~
~~~
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS</title>
    <style>
        body {background-color: purple;}
        h1 {color : blue;}
        p {color: red;}
    </style>
</head>
<body>
    <h1>가나다라바마사</h1>
    <h2>헤딩 태그</h2>
    <p>외부 스타일 시트는 많은 HTML 페이지의 스타일을 정의</p>
    </ol>
</body>
</html>
~~~
~~~
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>html</title>
    <style>
        table, th, td{
            border: 1px solid black;
            border-collapse: collapse;
        }
        th, td{
            background-color: #96d4d4;
            border-radius: 10px;
        }
    </style>
</head>
<body>
    <table>
        <tr>
            <th>Company</th>
            <th>Contact</th>
            <th>Country</th>
        </tr>
        <tr>
            <td>Samsung</td>
            <td>홍길동</td>
            <td>대한민국</td>
        </tr>
        <tr>
            <td>3M</td>
            <td>김일</td>
            <td>이노키</td>
        </tr>
    </table>
</body>

</html>
~~~
~~~
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>클래스 속성</title>
    <style>
        .city{
            background-color:aqua;
            color:white;
            border: 2px solid black;
            margin: 20px;
            padding: 20px;
        }
        .main{
            text-align: center;
        }
        #myHead{
        background-color:lightblue;
        color:red;
        }
    </style>
</head>
<body>
    <div class="city main">
        <h2>서울</h2>
        <p>서울은 한국의 수도이다.</p>
    </div>
    <div class="city">
        <h2>베이징</h2>
        <p>베이징은 중국의 수도이다.</p>
    </div>
    <div class="city">
        <h2>파리</h2>
        <p>파리는 프랑스의 수도이다.</p>
    </div>
     <div id="myHead">
        <h2>프랑크푸르트</h2>
        <p>프랑크푸르트는 독일의 수도이다.</p>
    </div>
</body>
</html>
#class 는 일괄적용 가능 id는 고유적용
~~~
~~~
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Wildcard selector</title>
    <style>
        *{background-color: gainsboro;}
        h1{color: red}
        p{color: blue;}
        body,h1,p,h3{margin: 50; padding: 10;}
    </style>
</head>
<body>
    <h1>로렘입숨이란</h1>
    <p>로렘 입숨(lorem ipsum; 줄여서 립숨, lipsum)은 출판이나 그래픽 디자인 분야에서 폰트, 타이포그래피, 레이아웃 같은 그래픽 요소나 시각적 연출을 보여줄 때 사용하는 표준 채우기 텍스트로, 최종 결과물에 들어가는 실제적인 문장 내용이 채워지기 전에 시각 디자인 프로젝트 모형의 채움 글로도 이용된다. 이런 용도로 사용할 때 로렘 입숨을 그리킹(greeking)이라고도 부르며, 때로 로렘 입숨은 공간만 차지하는 무언가를 지칭하는 용어로도 사용된다.</p>
    <br>
    <h3>그거 어디서 났어?</h3>
    <p>'로렘 입숨'</p>
</body>
</html>
~~~
~~~
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Class Selector</title>
    <style>
        .select{
            color: purple;
        }
        .select2{
            color: yellow;
        }
        .item{color: blue;}
        .header{background-color: rgb(11, 232, 55);}
    </style>
</head>

<body>
    <h1 class="item header">좋아하는 과일 이름</h1>
    <ul>
        <li class="select">사과</li>
        <li class="select2">복숭아</li>
        <li class="select header">귤</li>
        <li>딸기</li>
    </ul>
    
</body>
</html>
~~~
~~~
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>descendant css selectro</title>
    <style>
        #header h1{color: red;}
        #section h1,#section h2{color: blue;}
    </style>
</head>
<body>
    <div id="header">
        <h1 class="title">타이틀</h1>
        <div id="nav">
            <h1>네비게이션</h1>
            <h2>후손 적용 될까?</h2>
        </div>
    </div>
    <div id="section">
        <h1 calss="title">컨텐츠</h1>
        <h2>후손 적용 될까?</h2>
        <p>독자가 페이지의 레이아웃으 볼 때 페이지의 읽을</p>
    </div>
    
</body>
</html>
~~~
~~~
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>desc Table</title>
    <style>
        table > tr > th {
            color:red;
        }
        #class로 해줘야된다
        .color_r {color: blue}
    </style>

</head>
<body>
    <table border="1">
        <tr>
            <th class="color_r">이름</th>
            <th class="color_r">지역</th>
        </tr>
        <tr>
            <td>김삿갓</td>
            <td>파주</td>
        </tr>
        <tr>
            <td>홍길동</td>
            <td>방학동</td>
        </tr>
    </table>
    
</body>
</html>
~~~
~~~
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=, initial-scale=1.0">
    <title>Document</title>
    <style>
        div{
            width: 100px; height: 100px;
            background-color: red;
            border: 20px solid black;
            margin: 0,30px; padding: 0 30px;
        }
        .box{
            border-width: thick;
            border-style: dashed;
            border-color: black;
            margin: 20px; padding: 20px;
            border-radius: 20px 20px 0 0;
        }
    </style>
</head>
<body>
    <div class="box">
        <p>안녕하세요~ 반갑습니다.</p>
    </div>
</body>
</html>
~~~
~~~
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS font size</title>
    <style>
        .a{font-size: large;}
        .b{font-size: 32px;}
        .c{font-size: 1.5em; font-style: italic;}
        .d{font-size: 300%;}
    </style>
</head>
<body>
    <h1>Lorem Ipsum</h1>
    <p class="a">Lorem Ipsum</p>
    <p class="b">Lorem Ipsum</p>
    <p class="c">Lorem Ipsum</p>
    <p class="d">Lorem Ipsum</p>
</body>
</html>
~~~
~~~
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .f_big{font-size: 2em;}
        .f_italic{font-style: italic;}
        .f_bold{font-weight: bold;}
        .f_center{text-align: center;}
        .button{
            width: 160px; height: 80px;
            background-color: yellow;
            border: 10px solid black;
            border-radius: 30px;
            box-shadow: 5px 5px 5px #a9a9a9;
        }
        .button > a{display: block; line-height: 80px;}
    </style>
</head>
<body>
    <div class="button">
        <a href="#" class="f_big f_italic f_bold f_center">Click</a>
    </div>
</body>
</html>
~~~
~~~
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .box{
            width:200px; height: 200px;
            position: absolute;
        }
        .box:nth-child(1){
            background-color: red;
            left: 10px; top: 10px;
            z-index: 10;
        }
        .box:nth-child(2){
            background-color: green;
            left: 50px; top: 50px;
            z-index: 5;
        }
        .box:nth-child(3){
            background-color: blue;
            left: 100px; top: 100px;
            z-index: 1;
        }
       </style>
</head>
<body>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <h1>위치 속성 적용</h1>
</body>
</html>
~~~
~~~
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        img{float: left; width: 500px; height: 500px;}
    </style>
</head>
<body>
    <img src="kdg.png" alt="kdg">
    <p>김일은 박치기 왕이다</p>
    <p>김일의 잡!박!</p>
</body>
</html>
~~~
~~~
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .box{
            width: 200px; height: 200px;
            background-color: red;
            margin: 10px; padding: 10px;
            float: right;
            font-size: 3em;
        }
    </style>
</head>
<body>
    <div class="box">1</div>
    <div class="box">2</div>
</body>
</html>
~~~
~~~
f=open("D:\\41815042\\20230516\\singer1.csv",encoding='UTF-8')

s=f.readlines()
print(s,end="")

s=f.readline()
print(s,end="")

f.close()
~~~
~~~
with open("D:\\41815042\\20230516\\singer1.csv",encoding='UTF-8')as f:

    s=f.readline()
    print(s,end="")

    s=f.readline()
    print(s,end="")
~~~
~~~
def printList(pList) :
    for data in pList :
        print(data, end='\t')
    print()
with open("D:\\41815042\\20230516\\singer1.csv",encoding='UTF-8')as f:
    header = f.readline()
    header = header.strip()
    headerList = header.split(',')
    printList(headerList)
    for s in f:
        s= s.strip()
        rowList = s.split(',')
        printList(rowList)
~~~
~~~
#count
from tkinter import *

tk =Tk()
counter = 0

def clicked():
    global counter
    counter +=1
    label1['text'] = '버튼 클릭 수:' + str(counter)


def reset():
    global counter
    counter =0
    label1['text'] = '카운트 리셋'

tk.title('GUI 카운터')
label1 = Label(tk, text='옆에 버튼 있음', fg='blue', font=20)
label1.pack(side=LEFT, padx=10, pady=10)

#button
button1 = Button (tk, text='증가',bg='green', font=15,width=30 ,height=5,command=clicked)
button1.pack(side=LEFT,padx=10,pady=10)

button2 = Button (tk, text='리셋',bg='red', font=15,width=30 ,height=5,command=reset)
button2.pack(side=LEFT,padx=10,pady=10)

tk.mainloop()
~~~
~~~
