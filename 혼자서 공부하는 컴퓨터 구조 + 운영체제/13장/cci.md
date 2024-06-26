# 교착 상태란

## 식사하는 철학자 문제

- 교착 상태가 어떤 상황에서 발생하는지
- 교착 상태를 어떻게 해결할 수 있는지 알려주는 대표적인 문제 상황이다.

### 가정

- 탁자는 동그랗다.
- 다섯 명의 철학자가 있다.
- 다섯 명의 철학자 사이 사이에 포크가 있다.
- 식사를 하려면 포크 2개가 필요하다.

### 식사 순서

- 생각을 하다 왼쪽 포크를 집어든다.
- 생각을 하다 오른쪽 포크를 집어든다.
- 왼쪽과 오른쪽 포크 둘다 집어들게 되면 정해진 시간동안 식사를 한다.
- 식사 시간이 끝나면 오른쪽 포크를 내려놓는다.
- 그 다음은 왼쪽 포크를 내려 놓는다.
- 1번부터 다시 반복한다.

### 문제 발생

- 한 두명의 철학자가 식사를 하게 되면 아무런 문제가 없다.
- 단 서로가 동시에 왼쪽 포크를 집어들었을 때 문제가 발생한다.
- 왜냐하면 나의 왼쪽 포크는 곧 왼쪽에 있는 사람의 오른쪽 포크이기 때문이다.
- 철학자들은 이제 오른쪽 포크가 없기 때문에 오른쪽 포크가 나타날 때까지 생각하며 기다린다.
- 이렇게 일어나지 않을 시간을 기다리며 진행이 멈추는 것을 교착상태라고 한다.

### 다른 예시

- 게임 프로세스가 자원A를 사용 중
- 웹 브라우저 프로세스가 자원 B를 사용 중
- 게임은 자원 B를 웹 브라우저는 A를 써야 되는데, 자원이 빌 때까지 기다리고 있다면
- 이것이 바로 교착 상태이다.

## 자원 할당 그래프

1. 프로세스는 원, 자원은 사각형이다.
2. 사용할 수 있는 자원의 개수는 사각형 내 점으로 표현한다.
3. 프로세스가 어떤 자원을 할당받아 사용 중이라면 자원에서 프로세스를 향해 화살표로 표시한다.
4. 프로세스가 어떤 자원을 기다리고 있다면 프로세스에서 자원으로 화살표를 표시한다.

### 식사하는 철학자와 게임 프로세스와 웹 브라우저 예시를 보면

- 자원 할당 그래프로 표시하면 원의 형태를 그리고 있는 것을 볼 수 있다.

## 교착 상태 발생 조건

- 상호 배제
    - 하나의 자원을 하나의 프로세스만 사용할 수 있으므로 문제가 발생할 수 있다.
- 점유와 대기
    - 그냥 대기만 하면 괜찮은데, 자원을 할당받은 상태에서 다른 자원을 할당받기를 대기중이여서 문제가 발생할 수 있다.
- 비선점
    - 다른 프로세스가 점유한 자원을 빼앗을 수 있는 선점 상황이라면 모를까 빼았을 수 없고 자원을 사용중인 프로세스가 끝내길 무한정 기다릴 수 밖에 없는 상황이여서 문제가 발생할 수 있다.
- 원형 대기
    - 프로세스들이 원의 형태로 자원을 사용하기 위해 대기하는 것을 말한다.

# 교착 상태 해결 방법

## 교착 상태 예방

1. 상호 배제 삭제
- 모든 자원을 공유 가능하게 한다는 말
- 현실적으로 불가능에 가까움

1. 점유와 대기 삭제
- 한 프로세스에 자원을 몰아주거나, 없애버리거나 All or Nothing이 될 가능성이 크다.
- 그러므로 자원이 당장 필요해도 기다려야 하는 프로세스가 늘어날 수 밖에 없다.
- 자원의 효율성이 떨어진다.
- 더군다나 자원을 많이 사용하는 프로세스 같은 경우 자원을 적게 사용하는 프로세스에 비해 자원을 사용할 타이밍을 확보하기 어렵게 되고, 무한정 기다리게 되는 기아 현상이 발생할 수 있다.

1. 선점형으로 전환
- 한 자원을 빼았을 수 있는 선점형으로 바꿔보자.
- CPU 같은 자원은 프로세스들이 일정 시간을 두고 서로 공유하는 형태로 이용한다.
- 하지만 모든 자원이 선점 가능한 것이 아니기 때문에 범용성이 떨어진다.
- 예) 프린터

1. 원형 대기 삭제
- 자원에 번호를 붙이고 오름차순으로 배분한다.
- 왼쪽 포크를 집어들고 곧 바로 오른쪽 포크를 들지 않아도 되기 때문에 교착상태가 발생하지 않는다.
- 그런데, 모든 자원에 일일이 번호를 붙이는 것은 간단한 작업이 아니다.
- 그리고 각 자원에 어떤 번호를 붙이는 가에 따라서 특정 자원의 활용이 떨어질 수 있다.

**고로 예방 방식은 교착 상태가 발생하는 조건들을 제거하여 원천적으로 발생하지 않게 할 수는 있지만 여러 부작용이 따른다는 단점이 있다**

## 교착 상태 회피

- 교착 상태를 한정된 자원의 무분별한 할당으로 인해 발생하는 문제로 간주한다.

1. 안전 상태
- 안전 순서열이 있는 상태

1. 불안전 상태
- 안전 순서열이 없는 상태

1. 안전 순서열
- 교착 상태 없이 안전하게 프로세스들에 자원을 할당할 수 있는 순서

### 예시

- 할당 가능 자원 : 12개
- 할당한 자원 : 10개
- 남은 자원 : 3개

| 프로세스 | 최대요구량 | 현재 사용량 |
| --- | --- | --- |
| P1 | 10 | 5 |
| P2 | 4 | 2 |
| P3 | 9 | 2 |

안전 순서열 : P2 → P1 → P3

- 안전 순서열이 있는 상태에서의 최대 요구량을 원하는 최악의 상황을 가정
    - 순서
        - P2에게 남은 3개 중 2개를 몰아준다.
        - 자원을 4개 쓴 P2가 작업을 마치고 4개를 반환한다.
        - 이제 P1에게 남은 5개 중 5개를 다 몰아줘서 10개를 맞춰준다.
        - P1이 작업을 마치고 10개를 다 반환한다.
        - 남은 P3에게 7개를 주면 끝이난다.

### 예시2

- 할당 가능 자원 : 12개
- 할당한 자원 : 10개
- 남은 자원 : 3개

| 프로세스 | 최대요구량 | 현재 사용량 |
| --- | --- | --- |
| P1 | 10 | 5 |
| P2 | 4 | 2 |
| P3 | 9 | 3 |

- 안전 순서열이 없는 상태에서의 최대 요구량을 원하는 최악의 상황을 가정
    - 순서
        - P2에게 남은 자원 2개를 몰아줘서 최대 요구량을 맞춰준다.
        - P2가 작업을 끝마치고 자원 4개를 반환했다.
        - 그런데 어느 한 프로세스도 4개의 자원으로 최대 요구량을 만족치 못한다.
        - 그래서 P1과 P3는 서로 자원을 점유하며 오지 않을 상황을 바라고 무한정 대기한다.

## 교착 상태 검출 후 회복

- 교착 발생을 인정하고 사후에 조치하는 방식이다.
- 프로세스들이 자원을 요구할 때마다 그때그때 모두 할당한다.
- 교착 발생 여부를 주기적으로 검사한다.

### 회복 방법

1. 선점을 통한 회복
- 교착상태가 해결될 때 까지 한 프로세스씩 자원을 몰아주는 방식이다.
- 다른 프로세스들에게 자원을 빼앗아 몰아준다.

1. 프로세스 강제 종료를 통한 회복
- 한 프로세스씩 강제 종료
    - 작업 내역을 잃는 프로세스들을 최대한으로 줄일 수 있다.
    - 하지만 교착 상태가 없어졌는지 여부를 확인하는 과정에서 오버헤드 발생 야기
- 한 번에 다 종료
    - 가장 확실한 방법
    - 그러나 대다수의 프로세스들의 작업 내역을 잃게 될 가능성이 많다.

## 타조 알고리즘

- 무시