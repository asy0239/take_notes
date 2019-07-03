# lambda 함수

## 정의

- 함수를 정의하는 게 아니라 그 당시에만 쓰고 버리는 함수
- 다른 함수와 동시에 사용하면 좋다
- 밑에 그림을 보면 이해가 잘 됨

https://dojang.io/pluginfile.php/13854/mod_page/content/3/032001.png

```python
from functools import reduce
x = [1,2,3,4,5,6]
y = [1,2,3,4,5,6]
z = [1,5,6,3]
display(list(filter(lambda x: x % 2 == 0,x)))
display(list(map(lambda x,y: x+y, x,y)))
display(reduce(lambda x,y: x+y, z))
```

- reduce 는 내장함수가 아니라 불러와야 함, filter,map,reduce 말고도 많음
- reduce 는 [1,5,6,3] 이 들어가면 [(1,5),6,3] 으로 1,5 먼저 인자로 들어가며 다음엔 [(6,6),3]이런식으로 들어감

