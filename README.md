# claude-code-start

Claude Code 스킬과 에이전트를 학습하고 실험하기 위한 프로젝트입니다.

## 시작하기

### 1. 이 레포지토리 클론

```bash
git clone https://github.com/woodic/claude-code-start.git
cd claude-code-start
```

### 2. Anthropic 공식 스킬 레포지토리 참고하기

공식 스킬 예시를 별도 폴더에 클론해서 참고합니다:

```bash
# 참고용으로 별도 폴더에 클론
git clone https://github.com/anthropics/skills.git ../anthropic-skills-reference
```

또는 서브모듈로 추가하려면:

```bash
git submodule add https://github.com/anthropics/skills.git references/anthropic-skills
```

### 3. Claude Code에서 실행

```bash
# 프로젝트 폴더에서 Claude Code 실행
claude

# 또는 /init으로 CLAUDE.md를 자동 생성할 수도 있음
# (이미 CLAUDE.md가 있으면 개선점을 제안해줌)
```

## 프로젝트 구조

```
claude-code-start/
├── CLAUDE.md                          # Claude Code 프로젝트 설정
├── README.md                          # 이 파일
├── .claude/
│   ├── skills/                        # 커스텀 스킬
│   │   └── code-review-kr/
│   │       └── SKILL.md               # 한국어 코드 리뷰 스킬
│   └── commands/                      # 슬래시 커맨드 (추후 추가)
└── docs/                              # 학습 노트
```

## 스킬 만드는 법

### 기본 구조

```
.claude/skills/스킬이름/
├── SKILL.md          # 필수 — frontmatter + 지시사항
├── scripts/          # 선택 — 실행할 스크립트
├── references/       # 선택 — 참고 문서
└── assets/           # 선택 — 템플릿, 폰트 등
```

### SKILL.md 기본 템플릿

```yaml
---
name: my-skill
description: 이 스킬이 무엇을 하고, 언제 사용해야 하는지 기술합니다.
---

# 스킬 이름

스킬 지시사항을 여기에 작성합니다.
```

### 핵심 원칙: Progressive Disclosure

1. **frontmatter** (name + description) → 항상 로드됨 (~100 단어)
2. **SKILL.md 본문** → 스킬이 트리거될 때 로드
3. **scripts/references/assets** → 필요할 때만 로드

## 참고 자료

- [Anthropic 공식 스킬 레포](https://github.com/anthropics/skills)
- [Claude Code 공식 문서](https://code.claude.com/docs/en/skills)
- [Agent Skills 개요](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview)
- [CLAUDE.md 작성 가이드](https://claude.com/blog/using-claude-md-files)
- [Claude Code 베스트 프랙티스](https://code.claude.com/docs/en/best-practices)
- [커뮤니티 베스트 프랙티스 (20k+ stars)](https://github.com/shanraisshan/claude-code-best-practice)
- [Agent Skills 무료 코스](https://anthropic.skilljar.com/introduction-to-agent-skills)
