# Margin과 Padding의 차이
![image](https://user-images.githubusercontent.com/99263360/190116754-db891f1e-cb27-4d24-b43e-9f3019d69301.png)
- **Margin** : Object와 화면과의 여백(외부여백)으로 Border 바깥쪽을 차지한다. 주변 거리를 두기 위한 영역이다.
- **Padding** : Object 내의 내부여백으로 Content와 Border 사이의 여백을 차지한다. Content 영역이 배경 색이나 배경 이미지를 가질 때,  
Padding까지 영향을 끼친다. Padding은 Content의 연장으로 볼 수 있다.
- Margin 에만 **음수 값**과 **auto**를 적용할 수 있다.

***

### Margin과 Padding의 사용법
#### 1. 속성 4개 사용 시
- 위, 오른쪽, 아래, 왼쪽 순서로 값을 준다.  
ex) margin: 20px 10px 5px 10px
#### 2. 속성 2개 사용 시
- 상하 + 좌우 순서로 값을 준다.  
ex) margin: 20px 10px
#### 3. 속성 3개 사용 시
- 상하좌우에 같은 값을 한 번에 준다.  
ex) magin: 10px
#### 4. padding 속성 1개 사용 시
- 패딩의 1개 속성만 사용할 경우, 안쪽 여백이 변경된다.  
ex) padding: 10px
#### 5. 단일 속성 부여
- 어느 한 쪽에만 값을 부여하고 싶을 때, 방향을 직접 지정해주고 값을 부여하면 된다.  
ex) margin-top: 10px
#### 6. 가운데 정렬
- 가운데 정렬이 필요할 시, auto를 사용한다. padding에는 사용할 수 없다.  
ex) margin: auto
