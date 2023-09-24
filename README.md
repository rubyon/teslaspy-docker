# teslaspy-docker

git clone https://github.com/rubyon/teslaspy-docker.git

cd teslaspy-docker

docker-compose up -d

웹브라우저에서 http://%설치된 서버의 IP%:1267 로 접속한 후

테슬라 이메일 계정과 다른 부분을 설정 하시고 저장을 합니다.

Refresh Token 은

안드로이드폰은 https://play.google.com/store/apps/details?id=net.leveugle.teslatokens

아이폰은 https://apps.apple.com/us/app/auth-app-for-tesla/id1552058613

를 설치 하신 후 테슬라 아이디 로그인을 통해 Refresh Token 생성이 가능 합니다.

모든 설정이 끝나면 애프터블로우 기능을 이용 가능 합니다.

최초 아이디와 비번은 rubyon / password 입니다.

이 부분은 docker-compose.yml 에서 수정 가능하며 설정 없이도 사용 가능 합니다.

*네트워크 상태에 따라 간혈적으로 애프터블로우 시작과 종료가 안될수 있습니다.
네트워크가 연결되면 다시 시도하게 만들었으나 더블체크 부탁드립니다.


## 2023/09/24 23:00 업데이트 되었습니다.

docker-compose pull 명령어로 이미지를 새로 받아 컨테이너를 다시 생성해주세요.

- 보유 차량수를 6대에서 5대로 수정

## 이전 업데이트 내역.

- Refresh Token 영역 Textarea 태그로 교체 및 UI Round R 값 변경

- 불필요한 logging 주석처리

- Refresh Token 생성이 가능한 모바일 앱 링크 추가

- 설정 문구 추가

- 기존 로그인 방식을 refresh token 입력 방식으로 변경

- redis 비밀번호 제거 및 메인 컨테이너 네트워크모드 변경

- 비정상 종료 후 재실행 안되는 문제 해결

- 설정 문구 수정

- 운행종료시 공조기가 꺼져 있으면 애프터블로우 동작 안함 기능 추가

- 설정 문구 수정

- 운행종료시 공조기가 꺼져 있으면 애프터블로우 동작 안함 기능 추가

위 두 커밋을 원복 함.

- http auth 의 ID 와 PASSWORD 를 설정하지 않아도 실행 가능 하도록 수정

* 업데이트 후 이상동작을 한다면 모든 파일을 삭제후 git clone ... 명령부터 다시 해봐 주세요.

- 애프터블로우 동작방식을 기존 최대 온도로 동작시키고 설정온도로 돌아오는 부분을 성애제거 모드로 변경함

- 특정 온도를 설정하면 주행중 그 설정한 온도미만으로만 공조기가 동작했을 경우 애프터블로우가 동작함

- teslaspy_settings.json 버그 수정

- 애프터블로우 종료시 공조기 끄기

- 애프터블로우 종료시 공조기 끌때 버그 수정

- 개발 모드로 서비스가 실행되는 것을 프로덕션 모드로 실행되게 전면 수정 (docker-compose.yml 에 redis 컨테이너가 추가되어 다시 설치를 하셔야 합니다.)

- 차량을 충전할 때만 센트리모드를 켜는 설정 추가

- 사소한 문구 수정

- 리버스프록시로 도메인 연결시 action cable 동작 하도록 수정

설치에 어려움이 있으신 분들은

https://open.kakao.com/o/gtgDrDGf

오픈 채팅을 통해 지원 받으세요
