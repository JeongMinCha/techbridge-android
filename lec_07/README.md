# Lecture 7

## 수업 내용
1. XML 디자인 레이아웃에 대해서 배운다.
    - LinearLayout (Horizontal) vs LinearLayout (Vertical)
        - Horizontal로 하면 가로로 component 들이 나열된다.
        - Vertical로 하면 세로로 component 들이 나열된다.
    - layout:weight
        - LinearLayout 안에서 얼마만큼의 비율만큼 차지할지 결정
        - 예를 들어, 2개의 버튼을 같은 크기로 만들고 싶으면 둘의 비율을 1:1로 만들어준다.
            - 첫번째 버튼 클릭 후 layout:weight를 1로 설정
            - 두번째 버튼 클릭 후 layout:weight를 1로 설정
1. class variable에 대해서 배운다.
    - class 바로 아래에다가 쓰는 변수  
    - 여러 함수에서 동시에 쓰고 싶을 떄 써야 한다.  
    - class variable로 한 번 만들어두면 그 파일 안에서는 모두 사용할 수 있다.  
   ```
   public class MainActivity extends AppCompatActivity {
       ...
       // btnPlay, editTextHello는 전부 class variable이다.
       // 여기다가 쓴 변수는 모든 곳에서 쓸 수 있다.
       Button btnPlay;
       EditText editTextHello;
       ...
       public void onClick(View v) {
           if (v.getId() == R.id.btn_play) {
               // editTextHello 는 class variable이고,
               // onClick 함수에서 바로 사용할 수 있다.
               String res = editTextHello.getText().toString();
           }
       }
   }
   ``` 
1. 이미지를 안드로이드 프로그램에서 쓸 수 있는 방법을 배운다.
    - 이미지 파일을 준비한다. 그리고 이미지 파일들을 전부 ctrl + C 한다.
    - 안드로이드 스튜디오 안에서 app > res > mipmap 에서 ctrl + V 한다.
    - 이제, ImageView를 사용하면 추가했던 이미지들을 바로 사용할 수 있다.
    ```
    // 이미지를 추가한 후에는, 아래와 같이 ImageView에서 쓸 수 있다.
    imageViewMe.setImageResource(R.mipmap.left_scissors);
    imageViewCom.setImageResource(R.mipmap.right_rock);
    ```
1. 가위바위보 게임을 완성한다.
    - 레이아웃, 버튼 등을 다수 사용해서 이미지를 전부 보여주는 가위바위보 게임을 완성한다. (과제 내용을 참고)

## 과제
1. 실습때 완성못했던 가위바위보 게임을 완성한다.
    - 레이아웃 3개를 만든다.
        - 첫번째 레이아웃: TextView 2개
        - 두번째 레이아웃: ImageView 2개 -> 가위, 바위, 보 그림 나타내기
        - 셋번째 레이아웃: Button 3개 -> 가위, 바위, 보 버튼
        - play button: 버튼을 누르면 컴퓨터가 가위바위보를 랜덤하게 만들어내고, 사용자가 누른 버튼과 비교해서 가위바위보 게임을 한다.
        - TextView 1개: 가장 아래의 TextView로 결과값을 출력해준다.

## 다음 수업 내용
1. 완성한 가위바위보 게임에 점수 기능을 추가한다.
1. 작성한 코드를 인터넷에 올리는 방법을 배운다. (GitHub)
1. 딜레이 함수를 사용하여 시간차를 주어 가위바위보 게임을 좀 더 보강한다.
