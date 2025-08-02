# LTC-1.java

### 1. Two Sum(두 수의 합)

https://leetcode.com/problems/two-sum/

**문제 이해**

- 정수 배열 nums와 정수 target이 주어질 때,
  두 수를 더해 target이 되는 두 인덱스를 찾아 반환한다.

- 각 입력에는 정확히 하나의 답만 존재하며, 같은 원소를 두 번 사용할 수 없다.

- 반환 순서는 상관없다.

**접근 방법**

1. Brute Force (O(n²))

- 모든 쌍을 확인해 합이 target인지 검사한다.

- 구현은 간단하지만 시간 복잡도가 크다.

2. 해시맵 사용 (O(n))

- 배열을 한 번 순회하면서 (필요한 값: 인덱스)를 해시맵에 저장.

- 현재 값이 해시맵에 존재하면 바로 반환.

- 예: target - nums[i] 값을 먼저 찾고, 없으면 현재 값 저장.

<br>

# LTC-238.java

### 238. Product of Array Except Self(자신을 제외한 배열의 곱)

https://leetcode.com/problems/product-of-array-except-self/description/

**문제 이해**

- 정수 배열 nums가 주어질 때, 각 원소 i의 값이
  nums[i]를 제외한 모든 원소의 곱이 되도록 새로운 배열을 반환한다.

- 나눗셈을 사용하지 않고 O(n) 시간에 풀어야 한다.

**접근 방법**

왼쪽 곱과 오른쪽 곱 사용

- left[i] = i 왼쪽에 있는 모든 값의 곱

- right[i] = i 오른쪽에 있는 모든 값의 곱

- 최종 결과 = left[i] \* right[i]

<br>

# LTC-561.java

### 561. Array Partition(배열 파티션 1)

https://leetcode.com/problems/array-partition/description/

**문제 이해**

- 2n개의 정수가 주어질 때,
  배열을 n개의 쌍으로 나누고, 각 쌍의 작은 값들의 합이 최대가 되도록 한다.

- 그 최대 합을 반환한다.

**접근 방법**

1. **정렬 후 짝수 인덱스 합**

- 배열을 오름차순 정렬하면,
  (작은 값, 큰 값) 쌍에서 작은 값은 항상 짝수 인덱스에 위치.

- 따라서 모든 짝수 인덱스의 값을 더하면 최대 합을 구할 수 있다.

2. **이유**

- 큰 값을 작은 값과 묶는 것이 이득이므로, 정렬 후 인접한 값끼리 묶으면 최대가 된다.
