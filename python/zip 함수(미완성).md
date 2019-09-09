# zip 

zip은 내장함수이고 길이가 같은 자료형을 묶어 반환한다.

list, set, dict 함수 등을 같이 사용하여 결과를 반환한다.

## 함수 생성

```python
a = 'ahn'
b = [1,2,3]
c = ('하나','둘','셋','넷')

print(list(zip(a,b,c)))
print(set(zip(a,b,c)))
print(dict(zip(a,b,c)))
```

