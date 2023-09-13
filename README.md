# teslaspy-docker

git clone https://github.com/rubyon/teslaspy-docker.git

cd teslaspy-docker

docker-compose up -d

웹브라우저에서 http://ip.address:1267 로 접속한 후

테슬라 이메일 계정과 다른 부분을 설정 하시고 저장을 합니다.

이후

다시 도커가 설치된 터미널로 돌아와

docker exec -it teslaspy /app/venv/bin/python auth.py %email% 를 실행 합니다.

여기서 %email% 은 테슬라 계정 입니다.

이후 시키는 대로 인증을 마치면

애프터블로우 기능을 이용 가능 합니다.

최초 아이디와 비번은 rubyon / rubyon 입니다.

이 부분은 docker-compose.yml 에서 수정 가능 합니다.

*네트워크 상태에 따라 간혈적으로 애프터블로우 시작과 종료가 안될수 있습니다.
네트워크가 연결되면 다시 시도하게 만들었으나 더블체크 부탁드립니다.

* 2023/09/14 08:00 업데이트 되었습니다.

docker-compose pull 명령어로 이미지를 새로 받아 컨테이너를 다시 생성해주세요.

- 애프터블로우 동작방식을 기존 최대 온도로 동작시키고 설정온도로 돌아오는 부분을 성애제거 모드로 변경함

- 특정 온도를 설정하면 주행중 그 설정한 온도미만으로만 공조기가 동작했을 경우 애프터블로우가 동작함

- teslaspy_settings.json 버그 수정

- 애프터블로우 종료시 공조기 끄기 (추가)

* 업데이트 후 이상동작을 한다면 모든 파일을 삭제후 git clone ... 명령부터 다시 해봐 주세요.
