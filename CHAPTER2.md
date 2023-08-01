# 표현식 퍼즐

1. 홀수 확인

```java
return i % 2 == 1;
```

100% 로 홀수를 구할 것 같지만 그렇지 않음.

음수가 들어간경우 false를 리턴함.

이유는 자바의 % 연산자 정의 때문임.

`%`를 풀면 `(a / b) * b + (a % b) == a` 그리고 추가로 자바에서 정수를 나누면 버림을 수행하기 떄문임.

그럼으로 홀수를 구하기 위해서는 더 쉽게

```java
return i % 2 != 0;
```

로 구현하면 홀수를 확인할 수 있음.

더빠른 성능을 원하는 경우 비트 AND 연산자를 사용해 

다음과 같이 구현하면된다.

```java
return (i & 1) != 0;
```