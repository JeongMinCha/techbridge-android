# Lecture 4

## 수업 내용
- Toast 창 띄우기
    - Toast 창: 잠깐 떴다가 사라지는 창
    - 보통은 무언가 완료되었거나, 문제가 생겼을 때 Toast창을 띄워서 사용자한테 알려주도록 하는 경우가 많다.
    - 학생들도 버튼을 누른다음에 상태를 알려주고 싶다면 Toast를 띄워주는 것이 좋다.
- Control Structure: If statements (If문)
    - '~할때 ~하다'는 의미.
    - 특정 조건에서만 특정 동작을 하도록 만들 때 써야 한다.
        - <code> if (age > 10) {  
            Toast.makeText(MainActivity.this, "10살이 넘었네요!", Toast.LENGTH_SHORT).show();  
        } </code>
        - 이것은 age라고 하는 변수의 값이 10보다 클 때만 Toast창을 띄운다는 뜻이다.
    - 여러 조건을 연달아서 쓸 때는 if ~ else if ~ else if ~ else로 써야 한다.
- 정수를 문자열로, 문자열을 정수로 바꾸는 방법
    - 정수를 문자열로 바꿀려면:
        - <code>int a = 5;  
        String s = Integer.toString(a); // 이제 s는 값이 "5"이다.  </code>
    - 문자열을 정수로 바꿀려면:
        - <code>String s = "10";  
        int a = Integer.parserInt(s); // 이제 a는 값이 10이다.  </code>
- 실습
    - EditText, Button을 세개씩 만든다.
    - 각 3개의 component들은 이름, 나이, 전화번호를 의미한다.
    - 각 EditText마다 이름, 나이, 전화번호를 입력할 수 있게 만들어놓고
    - 각 버튼을 눌렀을 때 입력한 이름, 나이, 전화번호가 Toast창에 뜨도록 만든다.

## 과제

## 다음 수업 내용
