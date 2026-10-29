# Final Team Project

팀 프로젝트를 시작하기 위한 협업 저장소입니다. 기술 스택과 팀원별 담당 범위는 아직 결정되지 않았습니다. 현재 애플리케이션 코드와 실행 명령은 없습니다.

## 프로젝트 정보

- 팀 저장소: https://github.com/dudu110101/Final_Team_Project
- 통합 기준 브랜치: `main`
- 협업: 개인 포크 없이 이 저장소의 작업 브랜치에서 `main`으로 PR 제출
- 기본 병합 방식: 작업별 단기 브랜치는 Squash and merge
- 팀원에게 필요한 권한: 팀 저장소에 작업 브랜치를 push할 수 있는 쓰기 권한

## 처음 참여하기

관리자에게 쓰기 권한을 요청하고 초대를 수락한 뒤 저장소를 복제합니다. 권한이 없으면 포크로 우회하지 않고 로컬에서 작업하며 관리자에게 권한을 요청합니다.

```sh
git clone https://github.com/dudu110101/Final_Team_Project.git
cd Final_Team_Project
git switch main
git pull --ff-only origin main
git switch -c codex/short-task-name
```

작업마다 짧은 수명의 브랜치를 만들고 변경과 관련 문서를 함께 커밋합니다. 브랜치 이름은 기본적으로 `codex/작업명`을 사용하며, 팀에서 다른 규칙을 합의하면 함께 갱신합니다.

```sh
git add <변경한-파일>
git commit -m "변경 내용 요약"
git push -u origin codex/short-task-name
```

GitHub에서 **base: main**, **head: 작업 브랜치**, **대상: 이 팀 저장소**로 PR을 만듭니다. 변경 목적, 검증 결과, 미실행 항목을 PR 템플릿에 작성합니다. 검토만 요청된 PR은 임의로 수정하거나 병합하지 않습니다.

## 문서와 검증

- [작업 지침](AGENTS.md): Codex의 조사·검토·통합 기준
- [팀 합의와 결정 대기 항목](docs/team-agreement.md): 담당, 스택, 공통 계약, 검증 기준
- [PR 템플릿](.github/pull_request_template.md)
- [기본 저장소 검사](.github/workflows/repository-check.yml)

현재 CI는 공백 오류와 필수 문서 존재만 검사합니다. 애플리케이션 빌드·테스트를 검증하지 않습니다. 기술 스택을 정한 뒤 설치·실행·빌드·테스트 명령과 환경변수 예시를 이 README에 추가하고 해당 CI를 구성해야 합니다.

PR 검토 후 해결할 문제가 없고 필요한 검사가 충족되면 Squash and merge합니다. 문서의 협업 규칙은 GitHub 보호 규칙이 실제 적용되었다는 뜻이 아닙니다. 현재 권한·브랜치 보호·병합 옵션은 별도 설정 및 확인 대상입니다.
