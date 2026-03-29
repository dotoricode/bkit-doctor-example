# Step 2: init 후 상태

`bkit-doctor init --recommended`를 실행한 후의 상태입니다.
한 번의 명령으로 대부분의 bkit 구조가 자동 생성됩니다.

## 실행

```bash
bkit-doctor check
```

## 예상 결과

```
[bkit-doctor] 진단 대상: (현재 디렉터리)

──── 카테고리 ──────────────────────────
  ✓ structure   1 pass
  ✗ config      2 pass  1 fail
  ✓ docs        4 pass
  ✓ agents      1 pass
  ! skills      1 warn
  ✓ policies    1 pass
  ✓ templates   1 pass
  ✓ context     1 pass
  ✓ changelog   1 pass

──── 상세 ──────────────────────────────
[PASS] structure.claude-root — .claude/ 존재
[FAIL] config.claude-md — CLAUDE.md 없음 — 프로젝트 규칙 미정의
  없음: CLAUDE.md
  → CLAUDE.md 직접 작성 필요
[PASS] config.hooks-json — .claude/hooks.json 존재
[PASS] config.settings-local — .claude/settings.local.json 존재
[PASS] docs.plan — docs/01-plan 존재
[PASS] docs.design — docs/02-design 존재
[PASS] docs.task — docs/03-task 존재
[PASS] docs.report — docs/04-report 존재
[PASS] agents.required — 필수 agent 4개 모두 존재
[WARN] skills.required — skill 1개 SKILL.md 없음
  없음: .claude/skills/work-summary/SKILL.md
  → skill 디렉터리 + SKILL.md 생성 필요
[PASS] policies.required — 필수 policy 4개 모두 존재
[PASS] templates.required — 필수 template 4개 모두 존재
[PASS] context.required — .claude/context/ 존재
[PASS] changelog.exists — changelog 문서 존재

──────────────────────────────────────
총 14개 — PASS 12 / WARN 1 / FAIL 1   상태: FAILED
```

### 남은 항목

| 항목 | 상태 | 해결 방법 |
|------|------|-----------|
| `CLAUDE.md` | FAIL | 프로젝트 루트에 직접 작성 필요 |
| `work-summary` skill | WARN | `.claude/skills/work-summary/SKILL.md` 생성 필요 |

> `CLAUDE.md`는 프로젝트마다 고유한 내용이므로 `init`이 자동 생성하지 않습니다.

## 다음 단계

```bash
cd ../03-complete
```
