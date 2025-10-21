# Git Test Project

## 🧭 Branch Strategy
- `main`: 최종 배포용 브랜치
- `dev`: 통합 브랜치 (모든 PR은 여기로)
- `yunsujin`, `kimminji`, `parkjihun`: 개인 작업 브랜치

## 🧱 Workflow
1. 개인 브랜치에서 작업
2. `git add .` → `git commit -m "커밋 메시지"`
3. `git push origin [브랜치명]`
4. GitHub에서 **PR 대상 브랜치: dev**
5. 조장이 dev에서 통합 테스트 후 main으로 병합

## 💬 Commit Message Convention
- `feat:` 새로운 기능 추가  
- `fix:` 버그 수정  
- `style:` UI 및 코드 스타일 수정  
- `refactor:` 코드 리팩토링  
- `docs:` 문서 수정  
- `test:` 테스트 코드 추가  

## ⚙️ Local Environment Setup (using Conda)

모든 팀원이 동일한 개발 환경에서 FastAPI를 실행하기 위한 설정 가이드입니다.

### 🧱 Step-by-Step

```bash
# 1️⃣ Conda 환경 생성 (이름은 프로젝트에 맞게 변경 가능)
conda create -n gitTest python=3.10

# 2️⃣ Conda 환경 활성화
conda activate gitTest

# 3️⃣ 필수 패키지 설치
pip install fastapi uvicorn

# (필요 시 추가 패키지 예시)
# pip install numpy pandas scikit-learn

# 4️⃣ 현재 환경을 environment.yml로 저장
conda env export > environment.yml

# 5️⃣ 다른 팀원이 동일한 환경 생성 시
conda env create -f environment.yml

# (기존 환경 업데이트 시)
# conda env update -f environment.yml --prune

# 6️⃣ FastAPI 실행 테스트
uvicorn main:app --reload
