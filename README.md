# Universal Design v2.0.0

모델 및 공급사에 독립적인 제품 인터페이스 디자인 스킬입니다. 기존 모바일 앱 디자인 규칙을 유지하면서 웹과 데스크톱을 선택적으로 지원합니다. 특정 디자인 스타일, 모델, 프레임워크, 외부 서비스, API 키를 강제하지 않습니다.

## 설치 (macOS / Linux)

ZIP을 압축 해제한 뒤 실제 경로를 사용합니다. 다운로드 폴더에 압축을 푼 예:

```sh
npx skills add "$HOME/Downloads/universal-design" --skill universal-design
```

Codex 및 Claude Code에 전역 설치하는 예:

```sh
npx skills add "$HOME/Downloads/universal-design" --skill universal-design -a codex -a claude-code -g
npx skills list -g
```

다른 Agent Skills 호환 환경에서는 해당 환경의 설치 절차에 따라 폴더 전체를 복사합니다. SKILL.md와 references의 상대 경로를 유지하세요. 호환되지 않는 채팅 환경에서는 SKILL.md와 필요한 참조 문서의 내용을 직접 컨텍스트로 제공할 수 있습니다. 실제 스킬 지원 여부와 설치 경로는 호스트별로 다릅니다. CLI 문서: https://github.com/vercel-labs/skills/blob/main/docs/commands.md

## 사용 예시

- `universal-design 스킬로 기존 모바일 앱 디자인을 개선해. 기능을 유지하고 실행 및 스크린샷 검증이 가능하면 수행해.`
- `universal-design으로 데스크톱 PDF 뷰어의 문서 중심 레이아웃과 도구 모음을 개선해.`
- `universal-design으로 반응형 웹 대시보드를 설계해. 실제 데이터만 표시해.`
- `universal-design으로 현재 화면을 리뷰해. 코드 수정 없이 확인 가능한 근거와 개선 우선순위를 알려줘.`

## 모델 독립성

GPT 계열, Claude, Gemini, 오픈웨이트 모델 등 특정 모델에 종속되는 명령이나 서비스를 요구하지 않습니다. 다만 실제 에이전트가 스킬을 읽고 따를 수 있어야 하며, 코드 편집·실행·화면 분석 능력은 모델과 호스트에 따라 달라집니다. 이미지 분석이 불가능하면 시각 검증을 미실시로 기록하고, 실행 환경이 없으면 정적 검토만 수행합니다. 소형 모델은 필요한 참조 파일만 단계적으로 읽는 경량 절차를 사용합니다.

## 구성

- SKILL.md: 공통 디자인 규칙, 플랫폼 분기, 구현 및 검증 절차
- references/: 기존 모바일 가이드 11개 + 웹, 데스크톱, 에이전트 호환성 가이드
- evals/test-cases.md: 모델·스킬 간 비교용 수동 평가 시나리오 (실행 결과 아님)
- LICENSE / NOTICE: Apache-2.0 및 원본 출처

영어 지침을 사용하고 한국어 발동 조건 및 한국어 결과물 규칙을 포함합니다. 기존 프로젝트의 디자인 시스템과 데이터 계약을 우선합니다. 이전 gemini-mobile-design과 동시에 설치할 경우 중복 발동을 막기 위해 하나만 명시적으로 선택하거나 이전 버전을 제거하세요.

## 검증 범위

패키지 구조, 메타데이터, 참조 파일, ZIP 무결성을 정적으로 검증합니다. 실제 CLI 설치, 각 모델의 발동·지침 준수·디자인 품질 비교는 실행하지 않았습니다. evals 시나리오로 검증할 수 있습니다. 원본 스킬의 평가 결과는 이 스킬의 성능을 입증하지 않습니다.
