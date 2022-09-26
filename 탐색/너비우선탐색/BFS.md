# 1. 너비 우선 탐색이란?
- 완전 탐색 기법 중 하나
- 시작 노드에서 출발해 시작 노드를 기준으로 가까운 노드를 먼저 방문하면서 탐색하는 알고리즘
# 2. 너비 우선 탐색의 특징
- FIFO 탐색
- Queue 자료구조 이용
# 3. 너비 우선 탐색의 핵심 이론
1. BFS를 시작할 노드를 정한 후 사용할 자료구조 초기화하기<br>
![image](https://user-images.githubusercontent.com/94173023/192182120-4e1b2d3b-c9a2-4a4c-9073-bf4ac2bcac5e.png)
2. 큐에서 노드를 꺼낸 후 꺼낸 노드의 인접 노드를 다시 큐에 삽입하기<br>
![image](https://user-images.githubusercontent.com/94173023/192181884-cac48296-5bb4-4c4b-81fe-5a705cc0e2f8.png)
3. 큐 자료구조에 값이 없을 때까지 반복하기<br>
![image](https://user-images.githubusercontent.com/94173023/192182020-7a6ac5a0-95ee-4616-9104-1e0391901cb4.png)
# 4. 예시
* 백준
    * [DFS와 BFS 프로그램](DFS%EC%99%80BFS.md)
    * [미로 탐색하기](%EB%AF%B8%EB%A1%9C%ED%83%90%EC%83%89.md)
    * [트리의 지름 구하기](%ED%8A%B8%EB%A6%AC%EC%9D%98%EC%A7%80%EB%A6%84.md)