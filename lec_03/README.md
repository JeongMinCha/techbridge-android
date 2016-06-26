# Lecture 3

## 수업 내용
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

## 과제

## 다음 수업 내용
