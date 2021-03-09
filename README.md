# Study YouTube API
youtube api 연동 공부   
kotlin 사용

## YouTube Android Player API 사용 법
### API Download와 안드로이드 스튜디오에 적용
1. YouTube Android Player API 를 다운로드 받기. 
[API Download](https://developers.google.com/youtube/android/player/downloads?hl=ko)   
2. zip 을 풀고 .jar 파일을 프로젝트의 libs 안에 넣기
3. 안드로이드 스튜디오의 File > Project Structure > Dependencies로 이동
4. 사진에 체크한 + 버튼을 누르고 넣어두었던 .jar 파일을 추가   
![img1](https://user-images.githubusercontent.com/59243409/110480209-977b1400-8129-11eb-8f6e-607258b41662.png)
![img2](https://user-images.githubusercontent.com/59243409/110480395-cd1ffd00-8129-11eb-84b9-fd2077ad9689.png)
6. OK 버튼을 누르고 적용
### SHA-1 인증서 디지털 지문 알아내기
API KEY 를 등록할 때 필요하기 때문에 꼭 알아야 한다.   
학기 중에 배울때는 콘솔로 귀찮게 옮겨 다니며 찾았는데 이렇게 간단한 방법이 있었다.   
![img7](https://user-images.githubusercontent.com/59243409/110483965-9350f580-812d-11eb-9a3c-8f905cbfefca.png)
1. 안드로이드 스튜디오 오른쪽 상단 구석에 Gradle 클릭
2. 프로젝트 이름 > Tasks > android > signingReport 두 번 클릭
3. 화면 하단에 Run 화면을 보면 뭐가 죽 나오는데 거기서 SHA1: '000' 내용을 복사 ...
4. 그 후 API Key 발급 받을 때 사용량 제한 항목 추가에 SHA-1 인증서를 넣어주면 Key 사용 가능이다
### 제대로 사용하기 위해서(?) API KEY 발급받기  
Google APIs에 가서 API KEY를 발급 받아서 코드로 적용해야 사용 가능하다;;;
1. [Google APIs](https://console.developers.google.com/) 에 접속하고 로그인
2. 새로운 프로젝트를 만든다.
3. 사용자 인증 정보 > 사용자 인증 정보 만들기 > API 키 클릭   
![img3](https://user-images.githubusercontent.com/59243409/110481713-348a7c80-812b-11eb-962f-6b08b28cb374.png)
![img4](https://user-images.githubusercontent.com/59243409/110482137-acf13d80-812b-11eb-8292-c8406faedefe.png)
5. 키가 생성되면 키 값을 어디다 복사해두자 ... 앱에서 사용함
6. '이름' 부분을 클릭해서 들어간다.
7. 여기서 이름을 따로 설정해주고 싶으면 이름을 설정하고 일단 우리는 안드로이드 앱에 사용하는 거니깐 android 체크   
![img5](https://user-images.githubusercontent.com/59243409/110483324-f55d2b00-812c-11eb-994f-c1fc3648a7b8.png)
8. Android 앱의 사용량 제한에 새 항목을 추가하는데 이때 프로젝트의 패키지 이름(com.example.어쩌구)과 SHA-1 인증서를 넣고 완료를 누른다.   
![img6](https://user-images.githubusercontent.com/59243409/110483412-0ad25500-812d-11eb-8a27-9b1837cbf7cc.png)
9. 저장 하면 이제는 완전히 사용 가능

## 코드 설명
일단 유튜브에 올라와있는 코딩 방법을 참고한거라 설명이 불가능하다...   
Kotlin도 쌩 초보라 뭐가 뭔지 모르겠어🤣
