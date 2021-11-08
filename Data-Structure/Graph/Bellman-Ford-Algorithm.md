# 벨만 포드 알고리즘
그래프에 음의 가중치를 가지는 간선이 존재할 때 최단거리를 구하는 알고리즘

## 벨만 포드 알고리즘이란..

그래프 가중치에 음의 가중치가 존재한다면 다익스트라 알고리즘으로 제대로된 최단 거리를 찾을 수가 없다

### 이유

- 다익스트라 알고리즘 같은 경우에는 방문하지 않은 노드 중에 가장 최단 거리를 가진 노드를 방문하는 알고리즘 입니다 그러므로 특정 간선이 음의 간선을 가지고 있다면 해당 알고리즘에 반례가 생성됩니다 그러므로 음의 간선이 존재하면 다익스트라를 사용할 수 없다
- 음의 싸이클이 발생하게 되면 음수의 무한대의 값이 발생하고 이것은 그리디 방식을 취하는 다익스트라 알고리즘에서는 싸이클 존재 여부를 확인하지 못하기 때문에 잘못되었는지 판단 할 수가 없다

### 벨만 포드의 특징

- 벨만 포드는 그리디를 사용한 다익스트라와 다르게 모든 간선에 대한 경우의 수를 생각하기 때문에 앞에서 이야기한 문제들이 발생하지 않는다
- 벨만 포드 알고리즘이 음수 간선의 순환이 존재할 때 이것을 해결 할 수 있는 것이 아니라 순환이 존재하므로 제대로된 해를 만들 수 없음을 알려줄 수 있기 때문에 사용하는 것이다

### 시간복잡도

- 시간 복잡도가 O(VE)
- O(ElogV)를 가지는 다익스트라 보다 오래 걸린다

### 기본적인 로직

1. 최단거리를 담을 배열을 무한대로 초기화를 한다
2. 탐색을 시작할 정점을 0으로 선택을 한다
3. N-1 만큼 순회를 한다
    1. 모든 간선을 순회를 한다
    2. 출발 정점이 무한대가 아니라면 비용을 계산해서 최소비용으로 갱신한다
4. 싸이클 여부가 궁금하다면 1번 더 순회를 하면서 여기서도 갱신이 된다면 음의 싸이클이 존재여부를 판단 할 수 있다