# 🏁 kotlin-racingcar-precourse 🏎️

## [기능 요구 사항]

초간단 자동차 경주 게임을 구현한다.

- 주어진 횟수 동안 n대의 자동차는 전진 또는 멈출 수 있다.
- 각 자동차에 이름을 부여할 수 있다. 전진하는 자동차를 출력할 때 자동차 이름을 같이 출력한다.
- 자동차 이름은 쉼표(,)를 기준으로 구분하며 이름은 5자 이하만 가능하다.
- 사용자는 몇 번의 이동을 할 것인지를 입력할 수 있어야 한다.
- 전진하는 조건은 0에서 9 사이에서 무작위 값을 구한 후 무작위 값이 4 이상일 경우이다.
- 자동차 경주 게임을 완료한 후 누가 우승했는지를 알려준다. 우승자는 한 명 이상일 수 있다.
- 우승자가 여러 명일 경우 쉼표(,)를 이용하여 구분한다.
- 사용자가 잘못된 값을 입력할 경우 IllegalArgumentException을 발생시킨 후 애플리케이션은 종료되어야 한다.

## [구현 기능 목록]

### 1. 자동차 이름 입력 기능

- 경주할 자동차 이름을 받는다. 이름은 쉼표(,)로 구분한다. 이때 camp.nextstep.edu.missionutils.Console의 readLine()을 활용한다.

### 2. 이동 횟수 입력 기능

- 사용자가 몇 번의 이동을 할 것인지 입력 받는다.

### 3. 무작위 값 구하기 기능

- 0에서 9 사이의 무작위 값을 구한다. Random 값 추출은 camp.nextstep.edu.missionutils.Randoms의 pickNumberInRange()를 활용한다.

### 4. 전진 기능

- 무작위 값이 4 이상인 경우 전진한다.

### 5. 경주 기능

- 이동 횟수만큼 반복해 자동차끼리 경주하도록 한다.

### 6. 우승자 출력 기능

- 자동차 경주 게임 완료 후 누가 우승했는지를 출력한다. 우승자가 여러 명인 경우 쉼표(,)로 구분한다.

## [예외 처리 목록]

- 자동차 이름이 6자 이상인 경우: IllegalArgumentException 발생
- 자동차 이름이 빈 문자열일 경우: IllegalArgumentException 발생
- 자동차 이름에 이모티콘이 포함되어 글자 수가 더 많게 표현되는 경우: 이모티콘의 코드 포인트 수를 계산하도록 한다.
- 자동차 이름이 중복되는 경우: IllegalArgumentException 발생
- 이동 횟수가 양의 정수가 아닌 경우(문자열 또는 소수 또는 음수): IllegalArgumentException 발생
- 이동 횟수가 너무 많은 경우: 횟수 제한을 설정하고 제한을 넘길 시 IllegalArgumentException 발생