# Lecture 2

## 수업 내용
- 변수 개념
	- 변수: '값'을 담는 공간
	- '변할 수도 있는 값'을 담는 공간
- GUI Elements (디자인 요소)
	- EditText: 텍스트 입력을 하는 공간. 사용자가 텍스트를 입력할 수 있는 창이 생긴다.
	- TextView: 텍스트가 보여지는 공간. 일반적으로 정해져 있는 텍스트를 보여주는 역할을 한다.
	- Button: 버튼. 사용자가 버튼을 누르면 새로운 화면이 등장한다거나, 디자인 요소가 바뀐다거나 하는 반응을 만들 수 있다.
- TextView
	- setText: TextView에 보여지는 글자를 바꾸는 함수.
		- ex. textView.setText("");
- Button
	- OnClickListener
		- 버튼을 눌렀을 때 동작하도록 만들어주는 클래스.
		- public class ... 옆에 implements OnClickListener를 써준다. (두개가 뜨는데 반드시 android.view.View에 있는걸 써야 한다)
		- 그 줄에서 alt + enter를 치면 implement methods.. 와 같은 창이 뜬다. 그걸 선택하고 enter를 치면, onClick메서드가 만들어진다.
		- onClick 메서드를 만들고, 그 안에 button을 눌렀을 때의 동작을 쓰면 된다.
		- onClick 메서드 안에서는 v.getId()를 써서 어떤 버튼을 눌렀을 때 어떤 동작을 해야 하는지 쓴다.
		- if (v.getId() == R.id.name) 이렇게 쓰면 name이라는 id를 가진 요소가 클릭되었을 때, 그 뒤 과정을 수행하라는 뜻이다.

## 과제
버튼을 하나 더 새로 만들고, TextView에 있는 모든 글자들을 지우는 프로젝트를 만들어봅시다.

## 다음 수업 내용
- 주석 (코드 설명을 하거나, 코드를 생략시키도록 만들어주는 것)
- Toast 띄우기 (잠깐 글자가 떴다가 사라지는 창)
- primitive 타입 변수 배우기 (가장 기본적으로 쓰이는 변수들의 타입)
- Button 핸들링 다시 보기
