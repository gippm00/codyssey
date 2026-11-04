# 개발자 작업실 환경 구축 및 Docker 실습 보고서

## 1. 실습 환경
- OS: Windows 11 (WSL2 Ubuntu)
- Docker Version: Docker Desktop (WSL2 Integration)

## 2. 실습 진행 내용
1. Linux CLI 기초 명령어 실습 (폴더 생성, 파일 생성, chmod 755 권한 부여)
2. Docker Nginx 웹 서버 컨테이너 구동 및 포트 매핑 (8080:80)
3. Docker Volume을 활용한 데이터 영속성(Persistence) 검증 완료

## 3. 트러블슈팅 (Troubleshooting)
- **이슈 1:** WSL2 우분투에서 `docker` 명령어를 찾지 못하는 현상
  - **해결:** Docker Desktop 설정(Settings > Resources > WSL integration)에서 Ubuntu 연동 스위치 활성화.
- **이슈 2:** Dockerfile 경로 오타 및 빌드 캐시 문제
  - **해결:** `/usr/share/nginx/html` 경로 수정 및 `--no-cache` 옵션으로 이미지 재빌드 후 정상 웹 출력 확인.
