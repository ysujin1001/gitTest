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

예시:
