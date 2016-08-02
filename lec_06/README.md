# Lecture 6

## 수업 내용
1. 실습1: 가위바위보 게임
    - 가위바위보는 총 9가지 경우가 있다. 이 9가지 경우에 대해서 컴퓨터적인 사고(computational thinking)를 통해서 논리를 구조화할 수 있는지 배운다.
    - if문을 중첩되게 사용함으로써, 가위바위보 논리를 구현해낼 수 있다.
    ```
    if (me.equals("rock")) {
        if (com.equals("scissors")) {
            ....
        } ...
    } ...
    ```
1. 실습2: 주사위 굴리기
    - 버튼 1개
        - 버튼을 누르면 random하게 1~6중 임의의 값을 얻어 낼 수 있도록 한다.
        - 주어진 범위 내에 Random한 값을 출력해 낼 수 있어야 한다.
        ```
        Random random = new Random();
        int rand = random.nextInt(6); // 0~5까지의 임의의 값 도출
        rand = rand + 1; // 그 결과에 1을 더함으로써 1~6까지의 임의의 값이 됨
        ```
    - ImageView 1개
        - random하게 얻어낸 값을 가지고 주사위 화면을 보여준다.
1. 실습3: 계산기 만들기
    - 버튼 1개
        - '덧셈'을 수행할 수 있는 버튼
    - EditText 2개
        - 사칙연산에 대해서 두 개의 입력값
    - TextView 2개
        - 하나는 단지 'Answer'라고 하는 글자를 표현해주기 위한 것
        - 하나는 실제 계산 결과를 보여주는 텍스트 뷰

## 과제
1. 세번째로 다룬 '계산기 만들기' 프로젝트를 최종 완성시킨다. 실습시간에서는 '+'연산에 대해서만 계산기를 완성시켰으나, 덧셈, 뺄셈, 곱셈, 나눗셈 사칙 연산 전체에 대해서 계산기를 구현하여 완성하도록 한다.
이 때 반드시, add, subtract, multiply, divide 등의 이름으로 함수를 만들어서 구현해야 한다. 함수를 따로 만들지 않는 경우 과제를 제대로 하지 못한 것으로 간주한다.
    ```
    ...
    int left = Integer.parseInt(editTextLeft.getText().toString());
    int right = Integer.parseInt(editTextRight.getText().toString());
    int result = add(left, right);
    // + ""를 해준 이유는 정수를 문자열로 만들기 위해서!
    textViewAnswer.setText(result + "");
    ...
    
    public int add(int left, int right) {
        return left + right;
    }
    ```
1. 사칙연산 모두에 대해서 계산기 기능을 해야 하기 때문에 버튼을 총 4개를 만들어야 한다. 그리고 각 버튼이 눌려졌을 때
동작을 수행하려면 onClick함수에서 네 개의 버튼에 대한 처리를 해주어야 한다.  

    ```
    public void onClick(View v) {
        if (v.getId() == R.id.button_1) {
            ...
        }
        if (v.getId() == R.id.button_2) {
            ...
        }
        ...
    }
    ```

## 다음 수업 내용
1. 디자인: XML 레이아웃들
1. class variable이란 무엇인가
1. 이미지를 안드로이드 앱에서 사용할 수 있는 방법에 대해서 배운다.
1. 좀 더 완성적인 가위바위보 게임을 만든다.