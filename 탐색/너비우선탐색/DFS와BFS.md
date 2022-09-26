## 풀이법
### 슈도코드
```
N(노드 개수) M(에지 개수) Start(시작점)
A(그래프 데이터 저장 인접 리스트)

for M의 개수만큼 반복:
    A 인접 리스트에 그래프 데이터 저장

# 방문할 수 있는 노드가 여러 개일 경우에는 번호가 작은 것을 먼저 방문하기 위해 정렬
for N+1의 개수만큼 반복:
    각 노드와 관련된 에지를 정렬

# DFS 구현하기
DFS:
    현재 노드 출력하기
    visited 리스트에 현재 노드 방문 기록하기
    현재 노드의 연결 노드 중 방문하지 않은 노드로 DFS 실행하기(재귀 함수 형태)

visited 리스트 초기화
DFS(Start) 실행

# BFS 구현하기
BFS:
    큐 자료구조에 시작 노드 삽입
    visited 리스트에 현재 노드 방문 기록
    while 큐가 비어 있을 때까지:
        큐에서 노드 데이터를 가져오기
        가져온 노드 출력
        현재 노드의 연결 노드 중 미 방문 노드를 큐에 삽입(append 연산)하고 방문 리스트에 기록

visited 리스트 초기화
BFS(Start) 실행
```
### 나의 코드 구현
```python
```
## 남이 짠 코드
### 코드 구현
```python
from collections import deque
N,M,Start = map(int, input().split())
A = [[] for _ in range(N+1)]

for _ in range(M):
    s, e = map(int, input().split())
    A[s].append(e)
    A[e].append(s)

for i in range(N+1):
    A[i].sort()

def DFS(v):
    print(v, end=' ')
    visited[v] = True
    for i in A[v]:
        if not visited[i]:
            DFS(i)

visited = [False] * (N+1)
DFS(Start)

def BFS(v):
    queue = deque()
    queue.append(v)
    visited[v] = True
    while queue:
        now_Node = queue.popleft()
        print(now_Node, end=' ')
        for i in A[now_Node]:
            if not visited[i]:
                visited[i] = True
                queue.append(i)

print()
visited = [False] * (N+1)
BFS(Start)
```