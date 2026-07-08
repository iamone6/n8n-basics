# n8n-basics

n8n 컨테이너 실행을 위한 docker-compose 설정입니다.

## 실행

```bash
docker compose up -d
```

실행 후 브라우저에서 [http://localhost:5678](http://localhost:5678) 접속.

## 데이터

n8n 데이터는 `./n8n_data` 폴더에 bind mount 되어 저장됩니다.

## 환경변수

프로젝트 루트의 `.env` 파일이 `env_file`로 컨테이너에 주입됩니다. 워크플로우에 필요한 환경변수는 `.env`에 추가하면 됩니다 (`.gitignore`에 포함되어 커밋되지 않음).

`N8N_BLOCK_ENV_ACCESS_IN_NODE=false`가 설정되어 있어 Code 노드 등에서 `$env`로 환경변수 참조가 가능합니다.

## 종료

```bash
docker compose down
```
