# AIFFEL Campus Online 5th Code Peer Review Templete
- 코더 : 이진영
- 리뷰어 : 전재영


# PRT(PeerReviewTemplate) 
각 항목을 스스로 확인하고 토의하여 작성한 코드에 적용합니다.

- [O] 코드가 정상적으로 동작하고 주어진 문제를 해결했나요?
  
- [O] 주석을 보고 작성자의 코드가 이해되었나요?
  > 모든 부분에 주석이 잘 작성되어 있다.
- [O] 코드가 에러를 유발할 가능성이 없나요?
  > 제 수준에서는 없어보입니다.
  > 다른 미로를 테스트 해보았을때도 정상적으로 작동하였다.
- [O] 코드 작성자가 코드를 제대로 이해하고 작성했나요?
  > 코드상 정의 되어 있는 함수들의 기능들을 명확히 이해 했고
  > if 문을 통해 반복되는 원리도 이해했다.
- [O] 코드가 간결한가요?
  > 배운 내용상으로 가장 간결하게 작성한것 같다.

# 예시
1. 코드의 작동 방식을 주석으로 기록합니다.
2. 코드의 작동 방식에 대한 개선 방법을 주석으로 기록합니다.
3. 참고한 링크 및 ChatGPT 프롬프트 명령어가 있다면 주석으로 남겨주세요.
```python
# 사칙 연산 계산기
class calculator:
    # 예) init의 역할과 각 매서드의 의미를 서술
    def __init__(self, first, second):
        self.first = first
        self.second = second
    
    # 예) 덧셈과 연산 작동 방식에 대한 서술
    def add(self):
        result = self.first + self.second
        return result

a = float(input('첫번째 값을 입력하세요.')) 
b = float(input('두번째 값을 입력하세요.')) 
c = calculator(a, b)
print('덧셈', c.add()) 
```

# 참고 링크 및 코드 개선
```python
# 코드 리뷰 시 참고한 링크가 있다면 링크와 간략한 설명을 첨부합니다.
# 코드 리뷰를 통해 개선한 코드가 있다면 코드와 간략한 설명을 첨부합니다.
```
