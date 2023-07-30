> 이 곳은 prod 서버로 배포하기 위한 Repository입니다.
> 

## Branch 구조

- backend: 운영 서버로 backend를 배포하기 위한 레포지토리입니다.
- frontend: 운영 서버로 frontend를 배포하기 위한 레포지토리입니다.

## 배포 방법

1. Backend/Frontend/App 각 서버에서 main으로 push하면 테스트 서버로 배포됩니다.
2. QA 테스트 후 정상 작동되는 것이 확인되면 서브모듈을 업데이트합니다.
    ```java
    git submodule update --recursive
    ```
3. 업데이트 후 각 레포지토리에 push 하면 운영 서버에 배포됩니다.