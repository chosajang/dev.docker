
윈도우10 환경에서 WSL(Ubuntu) + docker를 설정하여 간단한 웹서버를 구축합니다

## docker-compose 관련 명령어
```
// docker-compose 실행
 - 실행 옵션
  > -d : 백그라운드 실행
  > --build : 빌드(docker-compose.yml 문서 변경 시, 옵션 적용을 위해 꼭 빌드옵션을 사용한다)
# docker-compose up -d --build

// docker-compose 종료
# docker-compose down

// 컨테이너 일부 재시작(*docker-compose 내용이 바뀐 경우에는 rebuild 해야함)
# docker-compose restart [컨테이너이름]
```

## docker 컨테이너 및 이미지 삭제명령어

```
// 컨테이너 전체목록 확인
# docker ps -a

// 컨테이너 전체 삭제
# docker rm `docker ps -a -q`

// 이미지 확인
# docker images

// 이미지 전체 삭제
# docker rmi `docker images -q`
```
