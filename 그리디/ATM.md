## 풀이법
### 슈도코드
```
```
### 시간 복잡도

### 나의 코드 구현
```python
import itertools
n=list(map(int,input().split()))

nPr = itertools.permutations(n, len(n))
print(nPr)

total=[]
for j in nPr:
    in_total = 0
    print(j)
    for k in range(len(j)):
        in_total += sum(j[0:k+1])
    total.append(in_total)
print(min(total))
```
## 남이 짠 코드
### 코드 구현
```python
n = int(input())  # 첫째줄 입력
peoples = list(map(int, input().split())) 
# 기다리는 사람들 리스트 형태로 입력 받음

peoples.sort()  # 작은 순서대로 정렬
answer = 0  # 정답 변수를 0으로 만듭니다.

for x in range(1, n+1):
    answer += sum(peoples[0:x])  # 리스트의 0번째 수부터 x번째 수까지를 더해줍니다.
print(answer)
```
```C

```
