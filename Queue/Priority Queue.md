우선순위 큐(Priority Queue)
=========
- 일반적인 큐는 FIFO(First In First Out)의 데이터 구조를 가진다.
- Priority Queue는 먼저 들어온 순서대로가 아닌 우선순위를 먼저 결정하고 
  그 우선순위가 높은 엘리먼트가 먼저 나가는 자료구조이다.
- 우선순위 큐는 힙을 이용하여 구현하는 것이 일반적이다.
- 데이터를 삽입할 때 우선순위를 기준으로 최대 힙 혹은 최소 힙을 구성한다.
- 데이터를 꺼낼 때 루트 노드를 얻어낸 뒤 루트 노드를 삭제할 때는 빈 루트 노드 위치에
  맨 마지막 노드를 삽입한 후 아래롤 내려가면서 적절한 자리를 찾아서 옮기는 방식으로 진행된다.
  
## Priority Queue의 특징
1. 높은 우선순위의 요소를 먼저 꺼내서 처리하는 구조 (큐에 들어가는 원소는 비교가 가능한 기준이 있어야함)
2. 내부 요소는 힙으로 구성되어 이진트리 구조로 이루어져 있음
3. 내부 구조가 힙으로 구성되어 있기에 시간 복잡도는 O(NLogN)
4. 응급실과 같이 우선순위를 중요시해야 하는 상황에서 쓰임


## Priority Queue 사용법
-java.util.PriorityQueue를 import 한 후, 
 Queue<Element> queue = new Queue<>()와 같은 형식으로 선언.
-기본은 우선순위가 낮은 숫자가 부여되고, 높은 숫자가 우선순위가 되게 하고 싶다면
  Collections.reverseOrder() 메서드를 활용한다.
  
  
  ex)Priority Queue 선언</br>
  import java.util.PriorityQueue;</br>
  
  //int형 priorityQueue 선언 (우선순위가 낮은 숫자 순)</br>
  PriorityQueue<Integer> priorityQueue = new PriorityQueue<>();</br>
  
  //int형 priorityQueue 선언 (우선 순위가 높은 숫자 순)</br>
  PriorityQueue<Integer> priorityQueue = new PriorityQueue<>(Collections.reverseOrder());</br>
  
  //String형 priorityQueue 선언(우선 순위가 낮은 숫자 순)</br>
  PriorityQueue<String> priorityQueue = new PriorityQueue<>();</br>
  
  //String 형 priorityQueue 선언 (우선 순위가 높은 숫자 순)</br>
  PriorityQueue<String> priorityQueue = new PriorityQueue<>(Collections.reverseOrder());</br>
  
  
# 힙(Heap)
 힙(Heap)은 우선순위 큐를 위해 고안도니 완전이진트리 형태의 자료구조이다.
 여러 개의 값 중 최댓값 혹은 최솟값을 찾아내는 연산이 빠르다.
 
 -힙의 특징
  완전이진트리 형태로 이루어져 있따.
  부모노드와 서브트리간 대소 관계가 성립된다.(반정렬 상태)
  이진탐색트리(BST)와 달리 중복된 값이 허용된다.
  
  ## 힙의 종류
  
    ##최대 힙(Max Heap)
    부모 노드의 키 값이 자식 노드보다 크거나 같은 완전이진트리이다.
   "key(부모노드) >= key(자식노드)"
    
  
  
  
    ##최소 힙(Min Heap)
    부모 노드의 키 값이 자식 노드보다 작거나 같은 완전이진트리이다.
   "key(부모노드) =< key(자식노드)"
