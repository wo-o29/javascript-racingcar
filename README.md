# javascript-racingcar

## 구현 할 기능 목록

1. 자동차 이름을 입력 받는다.

- 쉼표를 기준으로 나눈다.
- 이름의 앞, 뒤 공백은 제거한다.
- 이름은 1자 이상 5자 이하로 제한한다.
- 중복된 이름은 허용하지 않는다.
- 자동차의 개수는 1대 이상 10대 이하로 제한한다.
- 잘못된 입력을 받는 경우에는 에러 메세지를 출력한 후 해당 부분부터 다시 입력을 받는다.

2. 시도 할 횟수를 입력받는다.

- 정수가 아닌 숫자는 제한한다.
- 횟수는 1회 이상 100회 이하로 제한한다.
- 잘못된 입력을 받는 경우에는 에러 메세지를 출력한 후 해당 부분부터 다시 입력을 받는다.

3. 주어진 횟수 동안 n 대의 자동차는 전진 또는 멈출 수 있다.

- `실행 결과`라는 텍스트를 출력한다.
- 무작위 값은 0에서 9까지의 정수 값을 구한다.
- 무작위 값이 4 이상인 경우에만 전진한다.
- 전진한 결과 값을 출력한다.

4. 최종 우승자를 출력한다.

- 전진 횟수가 가장 높은 자동차를 구한다.
- 우승자가 여러 명일 경우 쉼표로 구분하여 출력한다.

## 폴더 구조

```
📦src
 ┣ 📂constants // 상수 메세지(에러, 출력)
 ┣ 📂utils // 랜덤 숫자 등
 ┣ 📂view // Input, Output
 ┗ 📜index.js // 진입점
```

## 🤔 고민사항들

Q. 입력을 받는 `readLineAsync` 함수는 utils 폴더에 넣어야 할까? view 폴더에 넣어야 할까?

> 정답이 없는 주제이다 보니깐 현재 코드 기준으로는 `src/view/input.js` 경로에 포함되어 있습니다!

- 아더: `readLineAsync` 함수는 입력 받는 코드에서 매번 가져다가 사용하는 함수이므로 utils에 들어가야 할 것 같다. view는 이러한 입출력 함수들을 사용하는 코드가 들어간다고 생각한다.

- 써밋: src 폴더 루트에 있는 utils 폴더는 관심사 구분 없이 조금 더 넓은 개념으로 어디서든 사용할 수 있을 것 같다는 느낌이 드는데(like es-toolkit 같은 느낌..?) 입력을 받는 `readLineAsync` 함수는 view 폴더 안에서만 사용될 수 있다보니깐 가까운 관심사에 두는게 응집도가 올라갈 것 같다.

Q. constants 폴더에 상수 범위가 그렇게 크지 않아서 한 파일에 다 넣었는데 이 때 파일명은 어떻게 하는게 좋을까요?

- index.js 보다는 constants.js가 좋을 것 같다 vs constants는 폴더 명에도 적혀있어서 index.js로도 충분할 것 같다
