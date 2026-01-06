# openuiweb

curl -v http://common.llm.domain.com/v1/chat/completions \
  -H "Authorization: Bearer <TOKEN>" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "gpt-4o-mini",
    "messages": [{"role":"user","content":"ping"}]
  }'
여기서 200 + JSON 나오면: 네트워크 아님 → OpenWebUI 설정/로그 레벨 문제 가능성 큼

여기서 400/404/405면: 서버가 OpenAI 호환이 “부분만” 되어 있거나 경로가 다름

여기서 401이면: 토큰/헤더 포맷 문제(아래 3번)

