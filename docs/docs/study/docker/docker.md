# 도커 기본 명령어

- 컨테이너 확인
```shell
docker ps
```

- 컨테이너 모두 확인
```shell
docker ps -a
```

- 컨테이너 삭제
```shell
docker rm [컨테이너 ID]
```

- 이미지 확인
```shell
docker images
```

- 이미지 삭제
```shell
docker rmi [이미지 ID]
```

- 컨테이너 이미지 같이 삭제
```shell
docker rmi -f [이미지 ID]
```

- Dockerfile 이미지 만들기
```shell
# -t: 이미지 이름 설정
docker build -t [이미지 이름] . 
```

- 이미지 작동시키기
```shell
# -d: 백그라운드 -p: 포트 --name: 컨테이너 이름 설정
docker run -d -p 3000:3000 --name [컨테이너 이름] [이미지 이름]
```
