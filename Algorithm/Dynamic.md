### 다이나믹 프로그래밍 (동적계획법)
- 메모리를 적절히 사용하여수행 시간 효율성을 비약적으로 향상시키는 알고리즘

- 이미 계산된 결과는 별도의 메모리 영역에 저장하여 다시 계산하지 않도록 한다.

- 최적 부분 구조
    - 큰 문제를 작은 문제로 나눌 수 있으며 작은 문제의 답을 모아서 큰 문제를 해결 할 수 있을 때

- 중복되는 부분 문제
    - 동일한 작은 문제를 반복적으로 해결

- 메모이제이션
    - 한 번 계산한 결과를 메모리 공간에 메모하는 기법이다.
    - 값을 기록해 놓는다는 점에서 캐싱이라고도 한다.

- 탑다운 vs 바텀업
    - 다이나믹 프로그래밍의 전형적인 형태는 바텀업이다.
        - 결과 저장용 배열를 DP 테이블이라고 한다.

### 다이나믹 프로그래밍 VS 분할정복
- 다이나믹 프로그래밍과 분할정복 모두 최적 부분 구조를 가질 때 사용 가능하다.(큰 문제를 작은 문제로 나눌 수 있고 작은 문제의 답을 모아서 큰 문제를 해결가능)
- 둘의 차이점은 부분 문제의 중복이다. 다이나믹 프로그래밍 문제에서는 각 부분 문제들이 서로 영향을 미치며 중복되는 것을 볼 수 있다.