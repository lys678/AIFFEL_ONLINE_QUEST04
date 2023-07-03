# AIFFEL Campus Online 5th Code Peer Review Templete
- 코더 : 이진영
- 리뷰어 : 박영수


# PRT(PeerReviewTemplate) 
각 항목을 스스로 확인하고 토의하여 작성한 코드에 적용합니다.

- [X] 코드가 정상적으로 동작하고 주어진 문제를 해결했나요?
  네 정상적으로 작동합니다.
- [X] 주석을 보고 작성자의 코드가 이해되었나요?
  > 네 마지막 출력부분에서 주석의 해설을 보고 이해 되었습니다.
- [X] 코드가 에러를 유발할 가능성이 없나요?
  > 네 스크립트가 변하지 않는한 결과값이 일치할 것 같습니다.
- [X] 코드 작성자가 코드를 제대로 이해하고 작성했나요?
  > 네 몇번의 질문을 통해 제대로 이해하고 있는지 확인했습니다.
- [X] 코드가 간결한가요?
  > 네 13줄로 무척 간결하게 작성하였습니다.

# 예시
1. 코드의 작동 방식을 주석으로 기록합니다.
2. 코드의 작동 방식에 대한 개선 방법을 주석으로 기록합니다.
3. 참고한 링크 및 ChatGPT 프롬프트 명령어가 있다면 주석으로 남겨주세요.
```python
import re                                # 정규표현식을 다루기 위한 파이썬 내장모듈 임포트
from google.colab import drive
from collections import Counter          #collections 모듈에 포함된 Counter 클래스 (이터러블한 데이터를 받아 각 요소의 개수를 카운트하고 딕셔너리로 받는다.)

#hello
def find_2grams(words):
    return [(words[i], words[i+1]) for i in range(len(words)-1)]       #리스트 컴프리헨션을 사용해 2-gram을 찾는 함수를 정의한다.


with open('/06TheAvengers.txt', 'r') as file: # 파일을 읽기형식으로 연다
    script = file.read().lower()            # 읽기형식으로 불러낸 파일을 소문자로 다 바꾼다.
    words = re.findall(r'\b\w+\b', script)  # 단어만 추출하여 리스트로 만든다.
    two_grams = find_2grams(words)          #find_2grams 함수에 소문자로 된 단어만 추출하여 만든 리스트 words를 넣어 2-gram을 찾고 그 리스트를 two_grams라는 변수에 할당한다.


counter = Counter(two_grams)                # Counter 클래스 사용한 two_grams를 counter 라는 변수에 할당한다.(Counter 클래스는 딕셔너리 형태로 출력한다.)
max_2gram, max_count = counter.most_common(1)[0]   #max_2gram은 counter.most_common(1)을 할당하여 제일 많이 나온 2_gram을 할당하고, max_counter는 횟수를 할당한다.

# 결과 출력
print(max_2gram, max_count)
print(counter)

```

# 참고 링크 및 코드 개선
```python
정규표현식의 다른 방법 
script = re.sub('[^a-zA-Z\s]', ' ', script)
을 통해 특수기호를 변경할 수 여백으로 변경할 수도 있습니다.
https://gocoding.tistory.com/93
```
