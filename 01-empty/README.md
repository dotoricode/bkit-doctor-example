# Step 1: 빈 프로젝트 진단

이 디렉터리는 bkit 구조가 전혀 없는 상태입니다.
`package.json`만 존재하며, `.claude/` 디렉터리나 관련 설정 파일이 없습니다.

## 실행

```bash
bkit-doctor check
```

## 예상 결과

```
[bkit-doctor] 진단 대상: (현재 디렉터리)

──── 카테고리 ──────────────────────────
  ✗ structure   1 fail
  ✗ config      2 warn  1 fail
  ! docs        4 warn
  ! agents      1 warn
  ! skills      1 warn
  ! policies    1 warn
  ! templates   1 warn
  ! context     1 warn
  ! changelog   1 warn

──── 상세 ──────────────────────────────
[FAIL] structure.claude-root — .claude/ 없음 — bkit 운영 환경 미설정
  없음: .claude
  → .claude/ 디렉터리 생성 필요
[FAIL] config.claude-md — CLAUDE.md 없음 — 프로젝트 규칙 미정의
  없음: CLAUDE.md
  → CLAUDE.md 직접 작성 필요
[WARN] config.hooks-json — .claude/hooks.json 없음 — hook 자동화 미설정
  없음: .claude/hooks.json
  → .claude/hooks.json 생성 필요
[WARN] config.settings-local — .claude/settings.local.json 없음 — 로컬 설정 미적용
  없음: .claude/settings.local.json
  → .claude/settings.local.json 생성 필요
[WARN] docs.plan — docs/01-plan 없음 — Plan 문서 미작성
  없음: docs/01-plan
  → docs/01-plan/ 디렉터리 생성 필요
[WARN] docs.design — docs/02-design 없음 — Design 문서 미작성
  없음: docs/02-design
  → docs/02-design/ 디렉터리 생성 필요
[WARN] docs.task — docs/03-task 없음 — Task 문서 미작성
  없음: docs/03-task
  → docs/03-task/ 디렉터리 생성 필요
[WARN] docs.report — docs/04-report 없음 — Report 문서 미작성
  없음: docs/04-report
  → docs/04-report/ 디렉터리 생성 필요
[WARN] agents.required — agent 4개 없음
  없음: .claude/agents/planner-orchestrator.md
  없음: .claude/agents/implementer.md
  없음: .claude/agents/phase-reviewer.md
  없음: .claude/agents/report-summarizer.md
  → agent 파일 스캐폴드 생성 필요
[WARN] skills.required — skill 7개 SKILL.md 없음
  없음: .claude/skills/phase-bootstrap/SKILL.md
  없음: .claude/skills/phase-plan/SKILL.md
  없음: .claude/skills/phase-design/SKILL.md
  없음: .claude/skills/phase-do/SKILL.md
  없음: .claude/skills/phase-check/SKILL.md
  없음: .claude/skills/phase-report/SKILL.md
  없음: .claude/skills/work-summary/SKILL.md
  → skill 디렉터리 + SKILL.md 생성 필요
[WARN] policies.required — policy 4개 없음
  없음: .claude/policies/global-policy.md
  없음: .claude/policies/output-policy.md
  없음: .claude/policies/security-policy.md
  없음: .claude/policies/documentation-policy.md
  → policy 파일 생성 필요
[WARN] templates.required — template 4개 없음
  없음: .claude/templates/plan-template.md
  없음: .claude/templates/design-template.md
  없음: .claude/templates/task-template.md
  없음: .claude/templates/report-template.md
  → template 파일 생성 필요
[WARN] context.required — .claude/context/ 없음 — 프로젝트 컨텍스트 미설정
  없음: .claude/context
[WARN] changelog.exists — changelog 문서 없음 — 변경 이력 미관리
  없음: CHANGELOG.md
  없음: docs/changelog.md
  없음: .claude/context/changelog.md
  → CHANGELOG.md 생성 필요

──────────────────────────────────────
총 14개 — PASS 0 / WARN 12 / FAIL 2   상태: FAILED
```

## 다음 단계

```bash
cd ../02-after-init
```
