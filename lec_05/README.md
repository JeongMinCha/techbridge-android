# Lecture 5

## 수업 내용
- 불 상수
    - 참/거짓을 말할 수 있는 것, 수학에서 '명제'랑 개념이 비슷하다.
    - AND 연산 => 모두 참이어야 참!
        - true AND true = true
        - true AND false = false
        - false AND true = false
        - false AND false = false
        ```
        if (age >= 20 && gender == 'M') {   // 나이가 20살보다 많고 남자면
        }
        ```
    - OR 연산 => 하나만 참이어도 참!
        - true OR true = true
        - true OR false = true
        - false OR true = true
        - false OR false = false
        ```
        if (age < 20 || gender == 'F') {    // 나이가 20살보다 어리거나 여자면
        }
        ```
- 복잡한 조건문 배우기
    - If ~ else if ~ else
        ```
        if (age < 10) {         // 나이가 10살보다 어리다면...
        } else if (age < 13) {  // 나이가 10살보다 어리지는 않으면서, 나이가 13살보다 어리다면
        } else if (age < 16) {  // 나이가 13살보다 어리지는 않으면서, 나이가 16살보다 어리다면 
        } else {                // 위 조건을 아무것도 만족 안한다면 (즉, 16살보다 어리지 않다면)
        }
        ```
    - 중첩된 If문 (If문 안에 If문)
        ```
        if (age > 20) {             // 나이가 20살보다 많다면
            if (gender == 'M') {    // 그리고 성이 '남자'라면
            }
        }
        ```
    - 중첩된 If문은 AND 연산으로 구현할 수도 있다!
        ```
        if (age > 20 && gender == 'M') {    // 나이가 20살보다 많고, 성이 남자라면
        }
        ```
- 함수
    - 특별한 입력을 줬을 떄, 특별한 출력을 주는 장치
    - 코드를 읽기 쉽게 만들고, 재사용 가능하게 만든다!
    - 아래와 같이 showErrorToast()와 같이 함수를 만들어 놓으면, 매번 Toast... 입력하지 않아도 showErrorToast()만 쓰면 Toast창을 띄울 수 있다!
    ```
    public void showErrorToast() {
        Toast.makeText(getApplicationContext(), "Error!", Toast.LENGTH_SHORT).show();
    }
    ```
    - 아래와 같이 showToastMessage함수를 만들면, 토스트 메시지를 다루게 줄 때도 함수를 써서 더 직관적으로 만들 수 있다.
    - 매번 Toast...와 같이 쓰지 않아도 직관적으로 토스트창을 띄울 수 있다.
    ```
    public void showToastMessage(String msg) {
        Toast.makeText(getApplicationContext(), msg, Toast.LENGTH_SHORT).show();
    }
    showToastMessage("Hello");
    showToastMessage("Hi!");
    showToastMessage("Error!");
    ```

## 과제
### 과제 1번
숫자를 받는 EditText 와 버튼을 만들고 0~100 사이의 숫자를 쓰고 버튼을 눌르면 토스트로

- 80점 이상이면 A
- 70점 이상이면 B
- 60점 이상이면 C
- 60점 미만이면 D  

를 보여주는 프로그램을 만들어라. 점수를 A~D 로 환산해서 토스트를 띄어주는 함수를 만들어서 프로그램을 만들어라.  
(반드시 토스트를 띄우는 함수를 따로 만들어서 구현할 것 어려우면 위에서 봤던 showToastMessage를 참고하시오)
### 과제 2번
네 과목의 점수를 입력받는 네 개의 EditText, 하나의 Button을 만들어라.  
그리고 네 개의 입력 점수의 평균값이 80점을 넘을 때 Toast로 합격했다고 보여지게 만들고,
평균값이 80점을 넘지 못하면 불합격했다고 보여지도록 만들어라.

## 다음 수업 내용
- 함수 (심화)
    - 함수의 입력에 대해서 (매개변수)
    - 함수의 출력에 대해서 (return)
    - 함수 안의 함수