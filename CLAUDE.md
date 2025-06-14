# CLAUDE.md

이 파일은 이 저장소에서 코드 작업 시 Claude Code (claude.ai/code)에게 가이드를 제공합니다.

## 프로젝트 개요

서버리스 마이크로서비스 아키텍처를 사용한 RealWorld 구현입니다. 현재 프로젝트는 기초 도구가 구성된 초기 개발 단계에 있습니다.

## MCP (Model Context Protocol) 설정

이 저장소는 `.claude/mcp.json`에 고급 MCP 서버들이 구성되어 있습니다:

- **puppeteer**: 브라우저 자동화 및 테스팅
- **TalkToFigma**: Figma 디자인 통합
- **taskmaster-ai**: Claude Sonnet 4를 활용한 AI 기반 작업 관리
- **github**: GitHub 저장소 운영
- **context7**: 문서 및 컨텍스트 관리
- **perplexity-ask**: AI 연구 기능

## 작업 관리

프로젝트 계획 및 작업 추적을 위해 taskmaster-ai MCP 서버를 사용하세요:
- `mcp__taskmaster-ai__initialize_project`로 프로젝트 초기화
- `docs/` 디렉토리의 PRD 문서를 파싱하여 작업 생성
- 작업 상태 업데이트로 개발 진행 상황 추적
- 기본 설정: 작업당 5개 하위 작업, 중간 우선순위

## 문서 구조

- `docs/example_prd.txt`: 프로젝트 개요, 기능, 아키텍처, 로드맵, 위험 평가 섹션이 포함된 한국어 PRD 템플릿
- 새로운 기능이나 프로젝트 단계 계획 시 이 PRD 템플릿을 사용하세요

## 개발 워크플로우

확립된 빌드 프로세스가 없는 새로운 저장소이므로:

1. **프로젝트 설정**: PRD 요구사항에 기반하여 taskmaster-ai를 사용해 프로젝트 구조 초기화
2. **아키텍처 계획**: 기술 아키텍처 결정을 위해 PRD 템플릿 구조를 따르세요
3. **작업 관리**: 기능을 관리 가능한 작업으로 분해하기 위해 taskmaster-ai를 활용하세요
4. **통합**: 저장소 운영 및 PR 관리를 위해 GitHub MCP 서버를 사용하세요

## 저장소 상태

새로 초기화된 저장소입니다. 빌드 도구, 테스팅 프레임워크 또는 CI/CD 추가 시:
- 적절한 설정 파일들을 생성하세요 (package.json, docker 파일 등)
- 특정 빌드 및 테스트 명령어로 이 CLAUDE.md를 업데이트하세요
- 코드베이스가 성장함에 따라 코딩 표준과 아키텍처 패턴을 확립하세요

## MCP 서버 환경

taskmaster-ai는 다음과 같이 구성되어 있습니다:
- 모델: Claude Sonnet 4 (claude-sonnet-4-20250514)
- Perplexity 모델: 연구용 sonar-pro
- 최대 토큰: 64,000
- 온도: 0.2 (집중적이고 결정론적인 응답)