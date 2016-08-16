# Lecture 8

## 수업 내용
1. 점수 기능 추가하기
    - Horizontal Linear Layout을 사용해서 현재점수와 최고점수를 나타내는 TextView 2개를 만들어준다.
    - 이길때마다 현재점수가 1점 올라가고, 비기면 점수가 변동이 없다. 하지만, 질 경우 바로 현재점수는 0점이 된다.
    - 이 때, 최고로 얻은 점수를 최고점수로 만들어준다.
    ```
    // 현재 점수가 이전의 최고 점수보다 높다면, 현재 점수를 최고 점수로 만들어 주자.
    if (curScore > maxScore) {
        maxScore = curScore
    }
    ```
1. 시간차를 주어 그림이 바뀌는 기능을 추가
    - 처음엔 둘 다 가위, 1초 뒤에 바위, 2초 뒤에 보를 보여주고
    - 마지막에 최종적인 가위바위보 결과를 보여주도록 구현한다.
    - 시간차를 주려면 Handler를 써야 한다.
    ```
    final Handler handler = new Handler();
    handler.postDelayed(new Runnable() {
        @Override
        public void run() {
            // 이 코드는 1초 후에 실행된다.
        }
    }, 1000);
    ```  
    - 핸들러가 실행되는 도중에 PlayGame버튼을 누르면 제대로 실행되지 않는다. play 버튼을 disable해주자.    


## 과제
1. 수업 시간에 다뤘던 가위바위보 게임의 시간차를 바꿔서 실행해본다. (예: 0.5초)
1. PlayGame 버튼을 disable하지 않고 실습을 마쳤는데, 이 버튼을 disable하도록 만들어서 완성해본다.  
```
// btnPlay를 누르지 못하게 만든다.
btnPlay.setEnabled(false);
```


## 다음 수업 내용
1. 배열이란?
1. 배열을 만들고 값을 세팅하는 방법과 값을 바꾸는 방법을 배운다.
1. 다양한 특성을 가진 배열을 만들어 본다.
1. 배열을 이용하는 ListView에 대해서 배운다.