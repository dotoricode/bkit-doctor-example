# bkit-doctor-example

[bkit-doctor](https://github.com/dotoricode/bkit-doctor)를 단계별로
체험할 수 있는 샘플 프로젝트입니다.

## bkit-doctor란?

AI 코딩 도구(Claude Code, Cursor 등)와 함께 사용하는 프로젝트의 구조를
진단하고 자동 보정하는 CLI 도구입니다.

## 준비

```bash
npm install -g bkit-doctor
```

## 단계별 체험

### Step 1: 빈 프로젝트 진단

```bash
cd 01-empty
bkit-doctor check
# → 대부분 FAIL/WARN
```

### Step 2: init 후 상태 확인

```bash
cd ../02-after-init
bkit-doctor check
# → 대부분 PASS
```

### Step 3: 완성 상태 확인

```bash
cd ../03-complete
bkit-doctor check
# → 14/14 PASS
```

## 직접 해보기

```bash
mkdir my-project && cd my-project
npm init -y
bkit-doctor check
bkit-doctor init --recommended
bkit-doctor check
```

## 관련 링크

- [bkit-doctor](https://github.com/dotoricode/bkit-doctor) — CLI 도구 본체
- [bkit-doctor npm](https://www.npmjs.com/package/bkit-doctor) — npm 패키지
- [bkit](https://github.com/popup-studio-ai/bkit-claude-code) — bkit 워크플로우

## License

MIT
