# Java Ladder
## 1주차 학습 계획
### 1단계
- [ ] 이중 배열을 다룰 경우 이중 for문 말고 다른 좋은 방법은 없나 찾아보기
- [x] Enum 활용하기
- [x] Input-Validation-Ladder-Encoding-Output 패턴으로 구현하기

### 2단계
- [ ] 리팩토링 개념 학습
- [ ] depth를 2 -> 1 로 변경하기 

### 3단계
- [ ] List, ArrayList, Generic 학습

### 4단계
- [ ] 단위 테스트 하기
- [ ] 객체지향생활체조원칙 학습
- [ ] 접근제어자 학습

## Mission. 사다리 게임 1단계 - 기본 기능 구현
### 미션 설계
1. Application 클래스
   - Controller 클래스에 의존
   - main 메서드 안에서 run()
2. Controller 클래스
   - Input 클래스에 의존
   - Validation 클래스에 의존
   - Ladder 클래스에 의존
   - Encoding 클래스에 의존
   - Output 클래스에 의존
   - run()
     - output.printMessageN()
     - input.intputN()
     - validation.validateInputN()
     - output.printMessageM()
     - input.intputM()
     - validation.validateInputM()
     - ladder.createLadder(int[])
     - encoding.encodeOutput(String[][])
     - output.printLadder(String)
- Input 클래스
  - inputN(), n을 입력받는다.
  - inputM(), m을 입력받는다.
- Validation 클래스
  - validationInputN(int) : n이 int형이 아니면 예외처리, n이 0보다 크지 않으면 예외처리
  - validationInputM(int) : m이 int형이 아니면 예외처리, m이 0보다 크지 않으면 예외처리
  - validationInputInteger(String)
  - validationInputPositive(int)
- Ladder 클래스
  - createLadder(int[])
    - createLadderEmpty(int[]) : String[m][n+2] 크기로 빈 배열 생성
    - makeLadderLength : 사람 수 만큼 '|' 로 세로를 채우기
    - makeLadderWidth : 가로 사다리 만들기
      - createRandomLadderWidth() : takeRandom()에서 반환된 값을 laddersFrame에 저장
        - LadderLine의 takeRandom()에서 랜덤으로 '-'나 ' '을 반환
  - String[][] 형으로 완성된 사다리 반환
- Encoding 클래스
  - encoding.encodeLadder(String[][]) : String[][]으로 받은 사다리를 String 형으로 반환
- Output 클래스
  - printMessageN : N 입력을 위한 메세지 출력
  - printMessageM : M 입력을 위한 메세지 출력
  - printLadder(String) : String으로 받은 사다리를 화면에 출력
- LadderLine Enum 클래스
  - stick : "-", blank : " "
  - takeRandom() : 랜덤으로 값을 반환

- Last Update: 2023-03-06

### 구현 결과
![ex1](https://user-images.githubusercontent.com/57451700/223053238-f18c4736-4bfa-447d-8523-7b41c78737da.png)    
![ex2](https://user-images.githubusercontent.com/57451700/223053325-ac5e56fc-ad65-4853-b21c-24ccdd033d0c.png)    
![result](https://user-images.githubusercontent.com/57451700/223053367-cc43a79e-c92a-4bfb-9d24-85f13e9e9c70.png)    


## 코드 리뷰

* [텍스트와 이미지로 살펴보는 코드스쿼드의 온라인 코드 리뷰 과정](https://github.com/code-squad/codesquad-docs/blob/master/codereview/README.md)

* [동영상으로 살펴보는 코드스쿼드의 온라인 코드 리뷰 과정](https://youtube.com/watch?v=lFinZfu3QO0&si=EnSIkaIECMiOmarE)
