# Lecture 12

## 수업 내용
- 액티비티란 무엇인가?
    - 안드로이드 프로그래밍에서 한 '화면'을 '액티비티'라고 부른다.
    - 하나의 화면은 최소 하나 이상의 java파일과 xml파일이 필요하다.
    - 다시 말하지만, java는 동작을 적는 곳이고, xml은 그림을 그리는 도화지이다!
- 새로운 액티비티 만들기
    - app > java > com..... > 에 보면 MainActivity가 있을 것이다.
    - 여기서 오른쪽 클릭하고 New > Activity > Empty Activity를 클릭해서 새로운 액티비티를 만들수 있다.
    - 실습 시간에는 LoginSuccessActivity라고 이름을 붙였다.
- 버튼을 눌러서 다른 액티비티로 이동하는 방법
    - onClick 함수를 만든다. (이미 많이 했던 것이므로 과정은 생략)
    - 원하는 버튼에 대한 onClick 메서드 안에, 아래와 같은 코드를 쓴다.
    ```
    Intent intent = new Intent(MainActivity.this, LoginSuccessActivity.class);
    startActivity(intent);
    ```
    - 여기서 intent 는 액티비티 이동을 의미하는 변수이다.
    - 액티비티 A에서 액티비티 B로 이동하게 만들려면, new Intent(A.this, B.class)와 같이 쓴다.
    - startActivity는 새로운 액티비티를 불러들이기 위한 함수이다.
- 실습 (로그인 프로그램)
    - 첫번째 메인 페이지 (MainActivity) 에서는 
    - 아이디, 비밀번호를 입력할 수 있는 EditText를 만들고,
    - 로그인을 하는 버튼을 만든다.
    - 두번째 페이지 (LoginSuccessActivity) 에서는
    - 로그인을 환영하는 TextView 정도를 만든다.
    - 그리고 여태까지 배웠던 버튼 핸들링을 이용해서, 아이디와 비밀번호가 맞을때만 두번째 페이지로 넘어가도록 어플리케이션을 만든다. 

## 과제
- 이전까지 만들었던 응용 프로그램들을 하나로 묶는 프로그램을 만들어보자.
- 메인 페이지에는 총 4개의 버튼을 만든다. 그리고 각각의 버튼을 클릭하면 이전에 만들었던 앱들을 띄워주는 형태로 앱이 동작하게 만들어보자.
- 첫번째 버튼을 누르면 FavoriteFood 프로그램을 띄워주고
- 두번째 버튼을 누르면 TimeTable 프로그램을 띄워주고
- 세번째 버튼을 누르면 RockScissorsPaper 프로그램을 띄워주고
- 네번째 버튼을 누르면 DiceRoll 프로그램을 띄워주자.

## 다음 수업 내용
- 연관배열이란 무엇인가? (HashMap)
- 액티비티의 원리
    - 액티비티는 하나씩 쌓여가는 형태가 된다.
    - 쌓여가는게 싫다면 액티비티를 직접 따로 없애야 한다.