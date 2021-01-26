### 수 자료형
- round() 함수를 사용해서 소수점 특정 자릿수에서 반올림 하도록 할 수 있다.
- 몫을 구하는 연산: //

### 리스트 자료형
- 빈 리스트 만들기: a[], a=list()
- 리스트 초기화 방법
    ```
    n=10
    a=[0]*n
    print(a)
    ```
- 인덱싱, 슬라이싱
    - a[-1]: 뒤에서 첫번째 원소 
    - a[-3]: 뒤에서 3번째 원소
    - a[1:4]: 2번째 원소부터 4번째 원소까지'
- 컴프리헨션
    ```
    array=[i for i in range(20) if i%2==1]
    ```
    - 2차원 배열 초기화할 때는 반드시 컴프리헨션을 사용하자.
    - N X M 크기 행렬 초기화
    ```
    n=3
    m=4
    array=[[0]*m for _  in range(n)]
    ```
- 기타 메서드
    - append(2)
    - sort(): 오름차순 정렬 sort(reverse=True): 내림차순 정렬
    - reverse: 리스트 원소 뒤집기
    - insert(2,3): 2인덱스에 3추가
    - count(3): 3인 데이터 개수
    - remove(1): 1삭제
- 리스트 원소 삭제
    ```
    a=[1,2,3,4,5,5,5]
    remove_set={3,5}
    result=[i for i in a if i not in remove_set]
    print(result)
    ```
### 튜플 자료형
- 소괄호()를 이용한다.
- 한번 선언된 값을 변경할 수 없다.

### 사전 자료형
- 키-값 쌍으로 테이터를 갖는다.
- 내부적으로 해시 테이블을 사용하여 데이터의 검색 및 수정이 빠르다.(O(1))
```
data=dict()
data['사과']='Apple'
data['바나나']='Banana'
data['코코넛']='Coconut'

```
- data.keys()로 키 데이터만 담은 리스트 사용가능
- data.values()로 값 데이터만 담은 리스트 사용가능

### 집합 자료형
- 중복을 허용하지 않는다.
- 순서가 없다.
- 초기화 방법: set 사용, 중괄호{} 사용
    ```
    data1=set([1,2,3,3,3,3,4,5])
    data2={1,2,3,3,3,3}
    ```
- 합집합: | 사용 ex) data1|data2
- 교집합: & 사용 ex) data1&data2
- 차집합: - 사용 ex) data1-data2
- add, update, remove 사용가능

### in, not in 연산자
- 리스트 안이나 여러개의 데이터를 담는 자료형에 사용할 수 있다.
```
a=[1,2,3,4,5,5,5]
remove_set={3,5}
result=[]
for i in a:
  if i not in remove_set:
    result.append(i)
print(result)
```

### 반복문 사용
- range(시작 값, 끝 값+1)
- range(10): 시작 값을 설정하지 않으면 0으로 설정된다.
```
for i in range(2,10):
  for j in range(1,10):
    print(i,"X",j,"=",i*j)
  print()
```

### 함수
```
def 함수명(매개변수):
    실행할 코드
    return 반환 값
```
```
def add(a,b):
    return a+b
```

### 입출력
```
n=int(input())
data=list(map(int,input().split()))

data.sort(reverse=True)
print(data)
```
- input()으로 입력받은 문자열을 split()을 이용해 공백으로 나눈 리스트로 바꾼 뒤에 map을 이용하여 해당 리스트의 모든 원소에 int() 함수를 적용한다. 그 결과를 list()로 바꿈으로써 입력받은 문자열을 띄어쓰기로 구분하여 각각 숫자 자료형이 된다.
```
import sys
data=sys.stdin.readline().rstrip()
print(data)
```
- sys 라이브러리를 사용할 때는 입력을 받고 rstrip() 함수를 공백 문자를 제거하기 위하여 사용한다.
- 숫자와 함께 출력
    ```
    a=7
    print('숫자'+str(7))
    print('숫자',7)
    ```
- 자릿수만큼 출력하기
    - %04d 라고 하면 999가 입력되면 0999로 출력된다.
    ```
    yyyy='%04d'%date[0]
    mm='%02d'%date[1] 
    dd='%02d'%date[2] 
    ```
- 문장 출력하기
    - str(input()) 사용
    - str(input())을 사용하면 배열로 바로 사용할 수 있다.
    ```
    str=str(input())
    for i in range(len(str)):
        print("'"+str[i]+"'")
    ```
- 연속해서 입력받기
    ```
    h, m, s = map(int, input().split(':'))
    print(m)
    ```
- N진수 입력받기(8진수), 출력하기
    ```
    num = int(input(), 8)
    ```
    - %를 사용하여 묶어서 표현한다.
    ```
    a=int(input(),16)
    for i in range(1,16):
        print('%X*%X=%X' % (a,i,a*i))
    ```
- 아스키코드와 숫자 변환
    - 아스키 -> 숫자
    ```
    num = ord(input())
    ```
    - 숫자 -> 아스키
    ```
    num = int(input())
    print(chr(num))
    ```

- 엔터 없이 출력하기
    - print에 end를 지정해준다.
    ```
    a= int(input())
    for i in range(1,a+1):
    if(i%3==0):
        continue
    print(i, end=' ')
    ```


## 비트 연산
- ~,&,|,^,<<,>> 가 있다.
```
int a=10;
printf("%d", a<<1); //10을 2배 한 값인 20 이 출력된다.
printf("%d", a>>1); //10을 반으로 나눈 값인 5 가 출력된다.
printf("%d", a<<2); //10을 4배 한 값인 40 이 출력된다.
printf("%d", a>>2); //10을 반으로 나눈 후 다시 반으로 나눈 값인 2 가 출력된다.
```