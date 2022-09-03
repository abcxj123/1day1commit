# PWA란?
- Progressive Web App은 일반적인 웹 기술로 구현된 Web App에 Native Mobile App(iOS, Android)만이 제공해왔던 app push,  
background sync 등의 주요 기능 등을 점진적(progressively)으로 적용하여 App을 향상시키는 것을 말한다.  
- 이제는 크롬을 비롯한 많은 부라우저들이 PWA 기능을 지원하기 때문에 웹 앱에서도 app push, background sync,  
offline에서도 동작하는 등의 다양한 기능을 사용할 수 있게 되었다.
- PWA는 2015년에 최초로 사용되기 시작하여 오늘날까지 사용자의 관심은 더욱 더 커져가고 있다.
***

### PWA의 장점 (Native Mobile App과의 비교)
#### 개발자 관점
Native App을 만들려면 플랫폼 환경에 맞는 언어(Android : Java, Kotlin / iOS : objective-C, swift)를 배워야한다.  
  
물론, Hybrid App(Web + App) 형태로 개발하면, 비교적 Native App 언어 비중이 적어지기는 하나 아예 없어지는 것이 아니다.  
  
flutter 등의 프레임워크를 이용하면 플랫폼에 상관없이 개발을 할 수 있으나 javascript에 익숙한 기존의 웹 개발자에게는 접근성이 높은 편이다.  
  
PWA는 다른 언어나 프레임워크를 필요로 하는 것이 아니라 javascript 1개의 언어로 플랫폼(iOS, Android)에 상관없는  
App을 만들 수 있어서 웹 개발자들이 쉽게 접근할 수 있으며, 기존에 개발된 Web App에도 쉽게 적용할 수 있다.  
  
또한, Vue.js, React.js, Ember.js, Angular.js 등의 client side framework에도 모두 PWA를 지원하기 때문에 손쉽게 PWA를 사용하여 개발을 할 수 있다.
#### 사용자 관점
Native App과 Mobile Web의 사용률을 비교한 통계 자료를 보면 Native App의 사용률이 Mobile web에 비해 6.7배 정도 높다고 한다.  
  
Native App에서 일반적인 Web App이 제공하지 않는 여러 기능을 제공하기 때문이다.  

하지만, Native App 사용자는 자신이 사용하는 주요한 App 몇 개만 주로 사용하며, 신규로 App을 설치하는 빈도는 매우 낮다.  
  
필요한 App을 store에 직접 들어가서 설치하는 과정이 매우 번거롭기 때문이다.  
  
  
그에 비해 PWA에서는 home screen icon 추가 기능(바로가기 아이콘 유사)을 제공하기 때문에 App store 접속없이 브라우저로 접근하여 손쉽게 App을 설치할 수 있다.  
  
웹서핑 도중 자연스럽게 App에 대한 노출도를 높임으로써 새로운 설치 가능성을 높여준다.  
  
또한, PWA는 Native App이 제공하는 대부분의 기능을 제공하기 때문에, PWA는 Mobile Web과 Native App의 장점을 모두 가졌다고 볼 수 있다.  
***
### PWA 핵심 기술
PWA가 제공하는 핵심 기술에는 다음과 같은 것들이 있다.
![image](https://user-images.githubusercontent.com/99263360/188277610-83a91420-d5a9-4406-b0eb-319b99db92d5.png)
- 출처 : https://www.happykoo.net/@happykoo/posts/173
