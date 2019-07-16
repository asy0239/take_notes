# map 과 apply

## 1. map

- 맵은 series 와 같은 index가 포함된 배열에 사용이 가능
- series의 값에 하나하나 접근하여 해당 함수를 수행
- iterable 한 배열, 자료에 사용한다

```python
import pandas as pd

data = {'team ' : ['russia', 'saudiarabia', 'egypt', 'uruguay']
        'against': ['saudiarabia', 'russia', 'uruguay', 'egypt'],
        'fifa_rank': [65, 63, 31, 21]}
columns = ['team', 'against', 'fifa_rank']
df = pd.DataFrame(data, columns = columns)

```

## 2. apply

- map 과 다르게 전체 column 에 해당 함수를 적용함
- 