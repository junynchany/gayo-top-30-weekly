# 가요 TOP 30 Weekly

한국 주간 인기가요 30곡을 영상과 함께 보여주는 정적 HTML 사이트와, 순위 선정에 사용하는 Codex 스킬을 함께 보관한 저장소입니다.

## 공개 사이트

<https://gayo-top-30-weekly.junynchany.chatgpt.site>

GitHub Pages: <https://junynchany.github.io/gayo-top-30-weekly/>

현재 포함된 차트는 **2026년 10월 1주차**입니다. 페이지 상단에서 년도·월·주차를 선택할 수 있으며, 저장되지 않은 기간은 데이터 준비 중으로 안내됩니다.

## 구성

- `dist/index.html`: 영상 30개와 기간 선택기가 포함된 사이트
- `.openai/hosting.json`: OpenAI Sites 정적 호스팅 설정
- `skill/gayo-top-10/SKILL.md`: 가요 TOP 10 Codex 스킬
- `skill/gayo-top-10/references/critique-rubric.md`: 비평 채점표
- `skill/gayo-top-10/agents/openai.yaml`: 스킬 UI 설정

## 로컬 실행

별도 빌드 과정 없이 `dist/index.html`을 브라우저에서 열거나 정적 파일 서버로 제공하면 됩니다.

`main` 브랜치가 갱신되면 `.github/workflows/pages.yml`이 `dist` 폴더를 GitHub Pages에 자동 배포합니다.

## 스킬 사용 예시

```text
$gayo-top-10을 사용해 이번 주 한국 인기가요 순위를 검토하고 근거가 포함된 최종 30곡을 선정해 주세요.
```

## 자동 갱신

매주 일요일 오후 6시(Asia/Seoul)에 최신 주간 순위를 조사합니다. 검증된 차트 데이터와 직접 재생 가능한 영상이 준비된 경우에만 `dist/index.html`을 갱신하고, GitHub Pages가 새 버전을 배포합니다.

