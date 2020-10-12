# We can use GitHub CLI 1.0
---
### 번역 사이트
* 매뉴얼
> ##### https://github.blog/2020-09-17-github-cli-1-0-is-now-available/
---
## 말하기에 앞서

    깃헙 CLI는 깃헙을 터미널로 가져옵니다.
    쉽게 스크립트를 작성하고, 고유한 작업을 만들어내고,
    작업 회귀를 해낼 수 있습니다.
    2020년도에 깃헙 CLI 베타를 발표했고, 
    이 이후 사용자는
    250,000개 이상의 pull을 하였으며,
    350,000개 이상의 merge를 하였으며,
    20,000개가 넘는 이슈를 만들었습니다.
    이제 깃헙 CLI는 베타가 아니며,
    윈도우, 맥, 리눅스에서 다운가능합니다.

## 깃헙 CLI를 사용하여 할 수 있는 것
- 터미널에서 이슈부터 이슈 해결까지 전체 깃헙 워크 플로우를 실행
- 깃헙 API를 호출하여 대부분의 작업을 스크립팅하고,
모든 명령에 대한 사용자 지정 별칭을 설정
- GitHub.com 외에 Github EnterpriseServer에 연결

발행에서 해제까지
전체 GitHub 워크플로우에 GitHub CLI를 사용합니다.

사용할 리포지토리 복제 gh repo clone owner/repo.
다음에 작업해야 할 사항 찾기 gh issue status 또는 gh issue list --assignee billygriffin.
Screenshot of GitHub CLI running 'gh issue list'

해당 기능을 추가하거나 버그를 수정했으면 gh pr create GitHub에서 꺼내기 요청을 만들 수 있습니다.
Screenshot of GitHub CLI running 'gh pr create'

그리고 당신의 팀 동료가 당신의 당기기 요청을 확인할 수 있습니다 gh pr checkout 1337, 다른 항목 보기 gh pr diff, 그리고 심지어 가벼운 리뷰를 제공합니다. gh pr review.
Screenshot of GitHub CLI running 'gh pr checkout 23' and 'gh pr diff'

당기기 요청이 승인되면 모든 테스트가 다음을 통해 통과되는지 확인할 수 있습니다. gh pr checks, 그리고 나서 터미널에서 바로 병합합니다. gh pr merge. GitHub CLI는 병합 후 로컬 및 GitHub.com에서 분기를 삭제할 수도 있습니다.
Screenshot of GitHub CLI running 'gh pr checks' and 'gh pr merge'

그리고 다음 릴리스를 자를 준비가 되면 그냥 사용하세요. gh release create [tag name] 그리고 명령줄을 벗어나지 않고 세상에 창조물을 제공할 수 있도록 하라!
GitHub CLI를 별칭 및 gh api
이제 GitHub CLI를 사용하여 모든 명령에 대한 별칭을 생성할 수 있습니다. gh alias set. 그리고 힘있는 자들과 함께. gh api GitHub API에 직접 액세스할 수 있도록 허용하여 사용자가 할 수 있는 작업에는 제한이 없습니다. gh명령어는 또한 쉽게 컴파일될 수 있다.

여기 팁이 있습니다: 당신의 별칭을 요지와 공유하기 위해서, 당신은 사용할 수 있습니다. gh alias list | gh gist create. GitHub CLI를 사용하여 별칭으로 작업할 수 있는 멋진 방법을 생각한다면 @github!

GitHub Enterprise Server에서 GitHub CLI를 사용할 수 있습니다.
마지막으로 GitHub Enterprise Server 2.20+에서 호스트된 리포지토리와 함께 GitHub CLI를 사용할 수 있습니다. 이것은 베타 발표 이후 가장 빈번한 요청이었고, GHES를 이용하는 사람들이 점점 더 많이 GitHub CLI를 이용할 수 있게 되어 기대됩니다.

너 없이는 할 수 없어
공동체는 깃허브에서 우리가 하는 모든 일의 핵심이다. NAT은 오픈 소스 리포지토리에 다음과 같은 기여와 함께 100개 이상의 커뮤니티 기여자를 보유하고 있습니다.

발급 및 꺼내기 요청 보기에 메타데이터 추가(감사합니다, @doi-t!)
빈 템플릿 선택 허용(감사합니다, @AliabbasMerchant!)
마일스톤, 언급 및 작성자(감사합니다, @eddumelendez!)별로 이슈 필터링
다른 생성 명령(감사합니다, @ShubhankarKG!)에 다시 생성 정렬
베타 기간 동안 보내주신 피드백을 기반으로 다음과 같은 기능을 제공합니다.

리포지토리 만들기 및 보기
SSH 및 기본 편집기를 사용하도록 GitHub CLI 구성
이슈 및 꺼내기 요청에 레이블, 피할당자 등을 닫았다가 다시 열었다가 추가합니다.
꺼내기 요청의 차이 보기, 검토 및 병합
우리는 매일 GitHub CLI를 더 잘 만들기 위해 여러분과 함께 일하게 되어 기쁩니다. 문제 편집 및 꺼내기 요청 지원, 설명 추가 등 향후 GitHub CLI 버전에 대해 많은 계획이 있습니다. 지금까지 본 모든 환상적인 아이디어와 콜라보레이션에 대해 정말 감사드리며, 앞으로도 많은 의견과 기여 부탁드립니다!
