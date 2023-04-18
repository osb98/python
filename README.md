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
~~~

