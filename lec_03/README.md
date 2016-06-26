# Lecture 3

## 수업 내용
- GUI elements 다루기
	- editText.getText().toString() => EditText에 입력한 것 가져오기
	- textView.setText(); => TextView에 문자열 등록하기.
- Button Handling (실습)
	- onCreate 함수 안에 findViewById로 XML버튼과 Java버튼을 연결시킨다.
	- 그 다음 줄에 button.setOnClickListener(this) 를 쓴다.
		- 이때, if (button != null) { ... } 로 감싸주어야 한다. 
	- MainActivity 옆에 implementes OnClickListener라고 치고, 자동완성되는 것들 중에서 android.view.View에 있는 것을 선택한다.
	- 아래에 onClick 이라고 하는 함수가 생긴다.
	- 그곳에 if (v.getId() == ...) { ... } 와 같이 쓴다.
		- ex. if (v.getId() == R.id.button_change)
- 변수란 무엇인가? primitive variables (기초 변수, 원시 변수)
	- 정수를 표현할 때는 int를 쓴다.
		- ex. int numStudents = 5;
	- 실수를 표현할 때는 double을 쓴다.
		- ex. double currency = 1170.05;
	- 문자열을 표현할 때는 String을 쓴다.
		- ex. String password = "hello";
- XML 디자인하기
	- XML 코드를 짜는 방법도 있지만, 'Design'창에서 끌어당겨서 만들 수도 있다.
	- Design창에서 EditText, TextView, Button을 만들 수 있어야 한다.
- 실습 수업
	- 실수를 입력하고 버튼을 누르면, 그 실수를 제곱한 값을 TextView에서 보여주도록 하는 앱을 만들었음.

## 과제
실수를 입력하고(EditText) 버튼을 누르면(Button) 그 실수에다가 +1한 값을 TextView에 보여주도록 하는 앱을 만든다.
여기서, 반드시 새로운 실수 변수를 쓴 다음에 setText를 써야 한다.
- double newNumber = Double.parseInt(editText.getText().toString()) + 1;
- textView.setText(newNumber);

## 다음 수업 내용
- Toast 띄우기
- 조건문이란? (if문)
- 유저에게 입력받기 (TextFields)
- 참/거짓의 개념을 알아보기.
- int를 String으로, String을 int로 할 수 있어야 한다.