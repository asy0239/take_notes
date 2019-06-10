# str.startswith() , str.endswith() 함수

문자열의 처음이나 마지막에 있는 텍스트를 매칭하는 간단한 방법

문자열 안에서 특정 텍스트를 찾는 방법은 여러가지인데

만약 내가 찾고 싶은 문자열의 형태가 문자열 처음에 있거나 마지막에 있다면

위 함수를 사용해서 쉽게 찾을 수 있다.

```
str = "this is string example....wow!!!";

print(str.startswith('this'))
print(str.endswith('wow'))
print(str.endswith('wow!!!'))
```

 