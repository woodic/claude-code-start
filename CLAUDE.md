# claude-code-start

Claude Code 스킬과 에이전트를 학습하고 실험하기 위한 프로젝트.

## 프로젝트 구조

- `.claude/skills/` — 커스텀 스킬 모음
- `.claude/commands/` — 슬래시 커맨드 모음
- `docs/` — 학습 노트, 참고 자료

## 주요 명령어

- `git add -A && git commit -m "메시지"` — 변경사항 커밋
- `git push origin main` — GitHub에 푸시

## 코드 스타일

- 한국어 주석 사용
- 파일명은 kebab-case (예: my-first-skill)
- SKILL.md의 description은 영어/한국어 혼용 가능

## 스킬 작성 규칙

- 스킬 폴더는 `.claude/skills/스킬이름/SKILL.md` 구조
- YAML frontmatter에 name과 description 필수
- description은 "언제 이 스킬을 사용해야 하는지"를 명확히 기술
- 큰 스킬은 scripts/, references/, assets/ 하위 폴더로 분리
- SKILL.md는 500줄 이하로 유지

## 주의사항

- .env 파일은 절대 커밋하지 않기
- API 키는 환경변수로 관리

