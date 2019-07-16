# datetime

- python 에서 날짜와 시간을 제공하는 datetime 모듈이다.
- 날짜와 시간 계산을 지원한다.

## 종류

```python
datetime.date # 날짜만 저장
datetime.time # 시간만 저장
datetime.datetime # 날짜와 시간을 저장
datetime.timedelta # 시간 구간 정보
datetime.tzinfo # 두 날짜, 시간 또는 날짜시간의 인스턴트 객체 간 차이를 마이크로 초 해상도로 나타내는 기간
detetime.timezone # tzinfo 추상 기본 클래스를 UTC의 고정 offset 으로 구현하느 클래스

```

## datetime.timedelta object

- 날짜나 시간사이의 구간을 나타낸다. 
- timedelta 에 들어갈 인자값

1주  : datetime.timedelta(weeks=1)

1일 : datetime.timedelta(days=1)

1시간 : datetime.timedelta(hours=1)

1분 : datetime.timedelta(minutes=1)

1초 : datetime.timedelta(seconds=1)

1밀리초 : datetime.timedelta(milliseconds=1)

1마이크로초 : datetime.timedelta(microseconds=1)

- 현재의 날짜와 시간을 문자열로 표현

```python
import datetime
 
now = datetime.datetime.now()
print(now)          # 2015-04-19 12:11:32.669083
 
nowDate = now.strftime('%Y-%m-%d')
print(nowDate)      # 2015-04-19
 
nowTime = now.strftime('%H:%M:%S')
print(nowTime)      # 12:11:32
 
nowDatetime = now.strftime('%Y-%m-%d %H:%M:%S')
print(nowDatetime)  # 2015-04-19 12:11:32
```

- 날짜, 시간형식의 문자열을 datetime 으로 변경 (strptime)

```python
myDatetimeStr = '2015-04-15 12:23:38'
myDatetime = datetime.datetime.strptime(myDatetimeStr, '%Y-%m-%d %H:%M:%S')
print(type(myDatetime)) # [class 'datetime.datetime']
print(myDatetime)       # 2015-04-15 12:23:38
```

- 날짜나 시간을 변경(replace)

```python
myDatetime = datetime.datetime.strptime('2015-04-15 12:23:38', '%Y-%m-%d %H:%M:%S')
print(myDatetime)   # 2015-04-15 12:23:38
 
yourDatetime = myDatetime.replace(day=16)  # year, month, day, hour, minute, second
print(myDatetime)   # 2015-04-15 12:23:38
print(yourDatetime) # 2015-04-16 12:23:38
```

