# 문제

1669 | 멍멍이 쓰다듬기
https://www.acmicpc.net/problem/1669

## 문제 풀이

구현 문제

1, 1 + 2 + 1(4), 1 + 2 + 3 + 2 + 1(9), 1 + 2 + 3 + 4 + 3 + 2 + 1(16) 이런식으로 최대 N의 키를 늘린다고 하면 최대 갖을 수 있는 차이는 N^2, 걸리는 날은 2\*N -1일

dif를 N^2로 차이를 줄여준 뒤 나머지 dif는 최대로 줄일 수 있는 값이 N이기 때문에 N으로 빼면서 값을 찾아줌

잘못 생각했던 부분은 dif가 남았을 때 날짜는 2*N-1일로 1,3,5,7일 이렇게 홀수 일만 있기 때문에 아래와 같이 마지막에 남은 dif에 대해 처리만 해주면 될 줄 알았는데 dif가 갖을 수 있는 최대값은 N*N - (N-1)*(N-1)로 2*N - 1이여서 두번까지 더 빼줄 수 있음
그래서 if문에서 while문으로 바꿔해결

```
if(dif > 0){
    answer++;
}
```
