# Lecture 9

## 수업 내용
1. 배열이란?
    - 여러 개의 원소를 나열한 것
    - 여기서 각 원소들은 타입, 형태가 같아야 한다.
    - 예를 들자면, 정수인 원소들이 총 5개인 배열이 있다. 등으로 말할 수 있다.
    ```
    int[] arr = new int[5]; // 정수인 원소가 5개가 있는 배열 하나
    ```
1. 배열을 만들고 값을 세팅하는 방법, 값을 얻어내는 방법을 배운다.
    - 배열을 만드는 방법
    ```
    int[] arr1 = new int[5];    // 길이만 지정해주는 방법
    int[] arr2 = {1,2,3,4,5};   // 처음부터 어떤 원소가 있는지 알려주는 방법
    ```
    - 배열의 원소에 값을 정하는 방법
    ```
    arr1[0] = 1;    // 배열은 항상 0부터 위치가 시작된다.
    arr1[4] = 5;    // 길이가 5인 배열은 마지막 위치가 4이다!! (중요)
    arr1[5] = 6;    // 에러가 난다. 왜냐하면 길이를 넘는 곳에 값을 썼기 때문이다.
    ```
    - 배열의 원소를 알아내는 방법
    ```
    // arr2[0] 를 그냥 쓰면 바로 arr2의 첫번째 원소의 값을 알아낼 수 있다.
    // 아래의 코드는 textView에 arr2의 값을 세팅하는 역할을 한다.
    textView.setText(Integer.toString(arr2[0]));
    ```
1. (심화) 이중배열이란?
    - 배열 안에 배열이 있는 것을 말한다.
    - 배열의 원소 자체가 배열이다.
    ```
    String[][] values = {
        // values의 첫번째 원소인 배열 (values[0])
        {
            "1교시",  // values[0]의 첫번쨰 원소인 String (values[0][0]) 
            "2교시"   // values[0]의 두번쨰 원소인 String (values[0][1])
        },
        // values의 두번쨰 원소인 배열 (values[1])
        {
            "3교시",  // values[1]의 첫번쨰 원소인 String (values[1][0])
            "4교시"   // values[1]의 두번쨰 원소인 String (values[1][1])
        }
    }
    ```
1. ListView에 배열을 붙여본다.
    - 맨 위에 있는 extends AppCompatActivity를 extends ListActivity로 바꿔야 한다.
    - XML에 ListView 요소를 하나 추가한다.
    - 그 ListView의 id는 기존과 달리 @android:id/list로 고쳐야 한다. (XML Text에 꼭 들어가야 한다!!!)
    - 아래와 같이 java코드에 치면 완성이다.
    ```
    String[] values = {"1교시", "2교시", "3교시"};
    ArrayAdapter<String> adapter = new ArrayAdapter<String>(this, android.R.layout.simple_list_item_1, values);
    setListAdapter(adapter);
    ```     


## 과제
1. 5개의 버튼을 추가하여, 각 요일별 자신의 시간표를 완성해본다. 
    - 버튼을 추가하여 버튼 핸들링하는 것이 아직 학생들이 어려워하므로 수업시간에 대부분 다뤘다.
    - 각 버튼별 핸들링하는 부분에다가 ListView 배열을 바꾸는 작업을 수행하면 된다. 

## 다음 수업 내용
1. Log.d란 무엇인가?
1. 반복문이란?
1. for-in 문이란?