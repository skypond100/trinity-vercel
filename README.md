# TRINITY — 사주 × 별자리 × MBTI 통합 분석

> 동양 명리학 · 서양 점성술 · MBTI 심리학을 하나로 통합한 성격 분석 서비스

---

## 🚀 Vercel 배포 방법 (5분 완성)

### 1단계 — GitHub에 올리기

```bash
# 이 폴더를 GitHub 레포지터리로 만들기
git init
git add .
git commit -m "TRINITY 첫 배포"

# GitHub에서 새 레포 만들고 연결
git remote add origin https://github.com/YOUR_USERNAME/trinity-app.git
git push -u origin main
```

### 2단계 — Vercel에 연결

1. [vercel.com](https://vercel.com) 접속 → **GitHub으로 로그인**
2. **"Add New Project"** 클릭
3. 방금 만든 GitHub 레포 선택 → **"Import"** 클릭
4. Framework: **Other** 선택
5. **"Deploy"** 클릭

### 3단계 — API 키 환경변수 설정 ⚡ (필수!)

1. Vercel 대시보드 → 프로젝트 선택
2. **Settings → Environment Variables** 이동
3. 아래 변수 추가:

| Name | Value |
|------|-------|
| `ANTHROPIC_API_KEY` | `sk-ant-...` (본인의 Anthropic API 키) |

4. **Save** 후 **Redeploy** 클릭

### 4단계 — 접속 확인

```
https://trinity-app-YOUR_USERNAME.vercel.app
```

---

## 📁 프로젝트 구조

```
trinity-app/
├── public/
│   └── index.html        ← 앱 전체 (사주·별자리·MBTI 분석)
├── api/
│   └── analyze.js        ← Anthropic API 프록시 (API 키 보호)
├── vercel.json            ← Vercel 라우팅 설정
├── package.json
└── README.md
```

---

## 🔑 Anthropic API 키 발급

1. [console.anthropic.com](https://console.anthropic.com) 접속
2. **API Keys** → **Create Key**
3. 생성된 키를 Vercel 환경변수에 입력

---

## ⚙️ 기능

- **절기 보정 만세력** — 24절기 기준 정밀 천간지지 계산
- **신살·귀인 분석** — 천을귀인, 월덕귀인, 도화살, 역마살 등 자동 탐지
- **별자리 자동 계산** — 생년월일 입력 시 태양궁 자동 판별
- **MBTI 인지기능 스택** — 주기능·부기능·3차·열등기능 분석
- **트리니티 수렴 엔진** — 3시스템 교집합 자동 추출, 모순 소거
- **역술인 장문 분석** — A3 4장 분량 7개 챕터 전문 풀이
- **가중치 고정 5:2:3** — 사주 50% · 별자리 20% · MBTI 30%

---

## 💰 비용 안내

- **Vercel** — 무료 플랜으로 충분 (개인 프로젝트)
- **Anthropic API** — 분석 1회당 약 $0.015~0.03 (Claude Sonnet 기준)

---

## 🛠️ 로컬 개발

```bash
# Vercel CLI 설치
npm i -g vercel

# 로컬 실행
vercel dev

# 환경변수 설정 (로컬)
echo "ANTHROPIC_API_KEY=sk-ant-..." > .env.local
```
