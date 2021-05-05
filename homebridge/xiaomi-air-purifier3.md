샤오미 공기청정기 종류가 매우 많은데 일반적인 모델들은 homebridge-mi-airpurifier ( https://github.com/YinHangCode/homebridge-mi-airpurifier ) 에서 잘 동작한다.

필자의 공기청정기는 3H 라서 별도의 방법을 찾아야 했다.

어느 친절한 외국인이 직저 플러그인을 만들어 주었다 :)  
homebridge-xiaomi-air-purifier3 ( https://github.com/rgavril/homebridge-xiaomi-air-purifier3 )

그래서 homebridge UI 에서 플러그인에 검색하고 설치하면 끝이다.  
그 다음에는 config.json 의 accessories 를 수정하면 된다 ( readme 문서 참고 )

문제는 샤오미 기기의 uid 와 token 값을 찾아야한다.  
여러 방법이 있지만 가장 손쉬운 방법으로는 node-mihome ( https://github.com/maxinminax/node-mihome ) 이 있다.

순서는 아래와 같다.
1. 미홈 앱 설치
2. 계정 국가를 us 로 설정
2. 공기청정기 추가
3. node-mihome 설치 및 실행 ( cloud MIoT 로그이 필수 )
4. option 에 국가르 us 로 변경
5. output 창에 기기의 uid, token 나옴

uid, token 값을 입력하고 config.json 저장 이후에 재시작을 하며 Homekit 에서 인식된다.
