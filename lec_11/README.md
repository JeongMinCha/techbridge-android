# Lecture 11

## 수업 내용
- for-in문의 한계, for 반복문의 이해
    - 0부터 9까지 숫자를 출력하려면... 저번 시간에 배웠던 for-in문으로 가능하다!
    ```
    int[] arr = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9};
    // arr에 있는 원소들 하나 하나를 element로 잡는다는 뜻이다.
    for (int element: arr) {
        Log.d("print", element);
    }
    ```
    - 하지만, 짝수 위치에 있는 원소들만 출력하고 싶다면? 그리고 순서를 거꾸로 출력하고 싶다면?
    - 우리가 기존에 배운 for-in문으로는 불가능하다!
    - for 반복문을 사용하면 가능하다
    ```
    for (int i = 1; i < 10; i += 2) {
        // 이렇게 하면, 짝수번째에 있는 원소들만 출력된다.
        Log.d("print", arr[i]);
    }
    ```
    - 여기서, int i = 1 은 반복문의 처음을 의미한다.
    - i < 10은 반복문의 조건을 의미한다. 즉, 이 표현이 맞을때까지만 계속 반복한다.
    - i += 2는 반복문이 실행된 후에 i가 바뀌도록 하는 작업을 말한다.
    - 즉, i값은 1부터 시작해서 2씩 증가하되, 10보다 작을때만 반복한다는 뜻이다.
    - 그러면 i는 1, 3, 5, 7, 9의 값을 가지게 되는데, 이 값은 짝수 번째의 위치를 나타낸다. (왜냐하면, 위치는 항상 0부터 시작되니깐)
- for 반복문을 사용하는 방법
    ```
    int[] arr = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9};
    for (int element: arr) {
        Log.d("print", element);
    }
    // i++ 는 1씩 증가시킨다는 뜻이다.
    for (int i = 0; i < 10; i++) {
        Log.d("print", arr[i]);
    }
    ```
    - 위에 있는 두 반복문은 완전 똑같은 말이다. (처음 원소부터 끝 원소까지 차례대로 출력)
    ```
    // i-- 는 1씩 감소시킨다는 뜻이다.
    for (int i = 9; i >= 0; i--) {
        Log.d("print", arr[i]);
    }
    ```
- array(배열) 의 한계, ArrayList의 이해
    - array(배열) 은 처음부터 길이를 지정해줘야 하고, 바꿀 수가 없다.
    - ArrayList를 쓰면 길이도 마음대로 바뀌고, 원소를 추가하고 삭제하고 마음 편하게 할 수 있다.
    ```
    // 여기서, ArrayList<String>이란 String(문자열)타입인 원소들을 가지는 ArrayList를 의미한다.
    // arr은 ArrayList의 이름이다.
    // new ArrayList<String>(); 는 이러한 ArrayList를 만들겠다는 뜻이다.
    ArrayList<String> arr = new ArrayList<String>();
    ```
- ArrayList 사용하기
    - ArrayList에 원소를 추가하기
    ```
    ArrayList<Integer> nums = new ArrayList<Integer>();
    nums.add(5);
    nums.add(4);
    nums.add(3);
    // 여기서 "" + nums는 nums를 문자열(String)로 만들겠다는 뜻이다.
    Log.d("print", ""+nums);
    ```
    - 원소를 가져올 수도 있다.
    ```
    // nums.get(2)는 위치 2(3번째 위치)에 있는 원소를 가져온다는 뜻이다. 여기서는 3을 가져올 것이다.
    Log.d("size", nums.get(2));
    ```
    - 원소를 설정할 수도 있다.
    ```
    // 위치 2 (3번째 위치)에 있는 원소를 7로 설정하겠다는 뜻이다.
    // 지금 {5,4,3}이었으므로 이것을 수행하고 나면, {5,4,7}이 된다.
    nums.set(2, 7);
    ```
    - 원소를 삭제할 수도 있다.
    ```
    // 위치 2 (3번째 위치)에 있는 원소를 지우겠다는 뜻이다. 이 이후에, {5,4}가 된다.
    nums.remove(2);
    ```
    - ArrayList의 크기를 알수도 있다.
    ```
    // 2가 출력된다. 왜냐하면 원소가 2개 있기 때문이다.
    Log.d("size", nums.size());
    ```
-  리스트 뷰 안에 있는 아이템이 클릭되었을 때 코드가 돌아가도록 한다.
    - onListItemClick 이라는 것을 쓴다.
    ```
    protected void onListItemClick(ListView l, View v, int position, long id) {
        super.onListItemClick(l, v, position, id);
        // 클릭한 아이템에 대한 정보를 가져온다.
        Object o = this.getListAdapter().getItem(position);
        int num = nums.get(position);
        // Dialog를 띄운다.
        AlertDialog.Builder alertDialogBuilder = new AlertDialog.Builder(this);
        AlertDialog alertDialog = alertDialogBuilder.create();
        alertDialog.setMessage("Clicked: " + num);
        alertDialog.show();
    }
    ```

## 과제
- EditText로 좋아하는 음식을 받아서 버튼을 누르면 좋아하는 음식 ArrayList 에 추가되어 추가될 때마다 
리스트를 AlertDialog 로 띄어주는 프로그램을 만들어라.
- 위에서 만든 프로그램에서 리스트뷰의 아이템을 클릭하면, 그 아이템을 삭제하는 프로그램을 만들어라. 이 때,
삭제된 아이템이 무엇인지 알려주도록 AlertDialog를 띄워 주어라.

## 다음 수업 내용
- 여태까지 만들었던 코드를 재활용할 수 있는 방법에 대해서 배운다.
- 어플리케이션에서 새로운 액티비티(화면)를 만들어서 띄워줄 수 있다.
