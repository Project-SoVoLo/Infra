# SoVoLo Infra (B-structure)
- 이 레포는 배포 오케스트레이션(Compose, Actions)만 담당합니다.
- 실제 소스는 병렬 폴더에 존재해야 합니다:

~/sovolo/
├─ Infra/         (이 레포)
├─ Backend/       (백엔드 레포)
├─ Frontend/      (프론트 레포)
└─ Chatbot/       (챗봇 레포)

## 사용법(EC2)
1) Infra/ 에 .env.prod 생성 (실 값 채우기) — 커밋 금지
2) Infra/secrets/에 sovolo_nlp_key_jy.json 배치 — 커밋 금지
3) docker compose -f docker-compose.prod.yml --env-file .env.prod up -d