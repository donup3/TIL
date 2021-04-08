### 이미지를 빌드하면서 캐시사용
- 이전에 빌드했던 Dockerfile에서 같은 내용이 있다면 build 명령어는 새로 빌드하지 않고 같은 명령어 줄까지 이전에 사용한 이미지 레이어를 활용해 이미지를 생성한다.
- git clone과 같은 명령어를 사용해 이미지를 build 한다면 build 명령어에 --no-cache 옵션을 추가해야한다. --no-cache 옵션을 추가하면 캐시를 사용하지 않고 처음부터 빌드를 시작한다.