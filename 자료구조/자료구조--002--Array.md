# Array
- 동일한 자료형의 데이터를 연속된 공간에 저장하기 위한 자료구조이다.
- index 0번부터 N-1번까지 데이터가 순서대로 저장된다.
- **배열의 길이는 고정되어 있다.**
- 변수의 선언을 줄여준다.
- 반복문 등을 이용하여 계산 과정을 쉽게 처리할 수 있게 도와준다.
***
### Array 선언
다음과 같이 배열을 선언한다.
```
int [] odds = {1, 3, 5, 7, 9};
int [] arr1 = new int[10];
String [] arr2 = new int[20];
```
***
### Array 값 사용하기
다음과 같이 배열의 값을 사용할 수 있다.
```
int [] nums = {1, 2, 3, 4, 5};
System.out.println(nums[2]); // 3
```
nums[2]는 nums 배열의 세 번째 데이터를 의미한다. (index는 0부터 시작하기 때문이다.)
***
### Array에 데이터 저장하기
다음과 같이 배열에 데이터를 저장할 수 있다.
```
int [] nums = new int[5];

for(int i=0;i<5;i++) {
  nums[i] = i+1;
}

for(int i=0;i<5;i++) {
  System.out.println(nums[i]); // 1 2 3 4 5
}
```
