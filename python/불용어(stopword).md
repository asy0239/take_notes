# 불용어(stopword)

갖고 있는 데이터에서 유의미한 단어 토큰만을 선별하기 위해 큰 의미가 없는 단어들을 제거하는 작업이 필요함

여기서 큰 의미가 없다는 건 너무 자주 등장해서 분석하는데 있어서 큰 도움이 되지 않는다라는 걸 말함

i, my , me , the 등 조사, 접미사 같은 단어들을 말하는 데 이러한 단어들을 불용어라 하며

NLTK에서는 위와 같은 단어들을 100개 이상 미리 정의해 놓음, 하지만 사용자가 설정가능하며 분석에 따라 불용어의 정의도 달라 질수있음.

## 1. NLTK에서 불용어 확인

```python
import nltk  
from nltk.corpus import stopwords  
stopwords.words('english')[:10]  

['i', 'me', 'my', 'myself', 'we', 'our', 'ours', 'ourselves', 'you', 'your']  

```

## 2. NLTK를 통해서 불용어 제거

```python
import nltk
from nltk.corpus import stopwords
from nltk.tokenize import word_tokenize

example = "Family is not an important thing. It's everything."
stop_words = set(stopwords.words('english'))#패키지에 미리정의된 영어불용어를 가져옴

word_tokens = word_tokenize(example)
result = []

for w in word_tokens:
    if w not in stop_words:
        result.append(w)
        
print(word_tokens) 
print(result) 


['Family', 'is', 'not', 'an', 'important', 'thing', '.', 'It', "'s", 'everything', '.']
['Family', 'important', 'thing', '.', 'It', "'s", 'everything', '.']
```

위 예시에선 is, not, an 이 제거 됨 It 같은 경우 제거가 안되나 봄

## 3. 한국어에서 불용어 제거

한국어는 konlpy 라는 패키지를 이용해 형태소 분석후에 조사, 접속사등을 제거하는 방법이 있다.

직접 정의해보는 이번엔 직접 불용어를 정의해 해보자.

```python
import nltk
from nltk.corpus import stopwords
from nltk.tokenize import word_tokenize

example = "고기를 아무렇게나 구우려고 하면 안 돼. 고기라고 다 같은 게 아니거든. 예컨대 삼겹살을 구울 때는 중요한 게 있지."
stop_words = "아무거나 아무렇게나 어찌하든지 같다 비슷하다 예컨대 이럴정도로 하면 아니거든"
## stop_words 는 직접 불용어를 정의한 것

stop_words = stop_words.split(' ')   ## 띄어쓰기를 기준으로 구분한다.

word_tokens = word_tokenize(example)
result = []

for w in word_tokens:
    if w not in stop_words:
        result.append(w)
        
        
        
print(word_tokens) 
print(result)



['고기를', '아무렇게나', '구우려고', '하면', '안', '돼', '.', '고기라고', '다', '같은', '게', '아니거든', '.', '예컨대', '삼겹살을', '구울', '때는', '중요한', '게', '있지', '.']
['고기를', '구우려고', '안', '돼', '.', '고기라고', '다', '같은', '게', '.', '삼겹살을', '구울', '때는', '중요한', '게', '있지', '.']
```

정의한 불용어 사전은 크게 좋은 결과를 주진 않는 것 같다. 하지만 자신이 무엇을 원하는지가 중요

https://www.ranks.nl/stopwords/korean 보편적인 불용어 사전 링크

