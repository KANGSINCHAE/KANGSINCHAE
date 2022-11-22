# Pull Request 개요
- 자신이 작업한 내용을 다른 사람들에게 공유 후 코드리뷰를 진행한 후 브랜치에 병합하는 과정을 의미
- 개발 팀원이 많을때, 프로젝트 규모가 클 때 많이 사용하게됨
- 개발회사에서 자주 사용하며 코드 리뷰의 기반이 됨

# 사용하는 이유
- 자연스러운 코드 리뷰가 가능하다
- 오픈 소스 프로젝트에 기여가 가능하다
- PR을 하면 Merge 전에 코드를 확인할 수 있고 각 코드별로 코멘트를 달 수 있다.
- Merge를 신중하게 할 수 있으며, Merge 할 때 팀원들이 확인하는 규칙을 정할 수 있다.
- 결국에는 코드의 안정성을 높일 수 있다.

# PR 생성 및 Merge 방법
- PR하기 전, 프로젝트를 가져와야 하며 새로운 Branch를 만들고, Commit -> Push 과정을 거쳐야 한다.
- PR은 자신이 한 작업을 기존 Main Branch에 병합하는 방법이기 떄문에 작업한 것이 있어야함
- 자신이 만든 Branch에서 Github에 Push까지 완료했다면 PR을 만들 수 있음.
- 우선 파일의 내용을 수정한 후, Contribute -> Open Pull Request를 클릭한다.
![image](https://user-images.githubusercontent.com/113485036/202963959-b71c6c89-6d76-4906-bb1d-a4bbf0d2cec5.png)
- 이후 Pull Request의 제목 및 설명을 기입한 후 Create Pull Request를 클릭한다.
![image](https://user-images.githubusercontent.com/113485036/202964137-097862ad-e5dc-495b-b8d0-de078e3dcc1c.png)
- 요청된 Pull Request를 확인하고 Merge Pull Request를 클릭하면 merge가 완료된다.
![image](https://user-images.githubusercontent.com/113485036/202964514-d24af765-b9a6-4936-a627-8335e5d9e31a.png)

# Merge의 종류
- Merge Pull Request를 하는 방식에는 merge commit을 만드는 방법, squash and merge, rebase and merge 같이 3가지 방법이 있다.  
![image](https://user-images.githubusercontent.com/113485036/202966170-09b8d11d-b6e6-49b9-a329-89f6ded889fe.png)

### Create a merge commit
- 흔히 알고 있는 일반 병합이며, 그대로 합쳐지고 git histroy에도 합쳐지는 그래프가 나옴
- 장점은 history에서 자세한 과정을 확인할 수 있음
- 단점은 branch가 매우 많아질 수 있으며 복잡한 history 그래프가 그려질 수 있다는 것
- 프로젝트 규모가 크고 많은 사람들이 브랜치를 만들어서 사용할 때는 사용하지 않는 것이 좋음

### Rebase and Merge
- 합치고자 했던 Branch의 commit들을 그대로 base branch로 옮겨준다.
- 일반 Merge처럼 합치는 것이 아닌 commit 내역을 그대로 떠서 옮겨준다.
- git history상에는 그래프가 합쳐지진 않고 base만 위로 올라가면서 갱신된다.
- 장점은 git history를 깔끔하게 볼 수 있다.
- 단점은 여러 commit을 rebase merge할때 충돌이나면 merge하려던 모든 커밋에서 충돌이 발생한다.
- 이때문에 의미없는 커밋이 history에서 계속 남게 된다.

### Squash and merge
- Rebase merge에 옵션이 붙은 merge이다.
- rebase를 진행하고 merge할 commit들을 하나의 commit에 합친다. squash merge를 하면 많은 commit들을 하나의 commit에 합쳐
깔끔한 Git History가 나오게 한다.
- 자잘한 commit이 많을 때 깔끔하게 history를 정리할 때 추천한다. 하나의 commit에 의미없는 commit들도 합쳐주기 때문

# 결론
- PR은 여러 장점을 가지고 있는 Process이므로 위와같은 방식으로 merge를 진행하여 라이브 제품을 배포할 때는 위의 과정을 필수로 거침.
- 개발망이나 테스트용 branch에 Merge 할 때에는 생략하고 Local Merge를 진행하기도 함.

# 사용 평가
- Pull Request를 사용하면서 소스코드의 병합 사항을 한눈에 확인할 수 있었음
- 최종 병합 시 충돌이 발생하는 경우는 결국엔 사용자가 직접 병합해야 하는 점은 아쉬움으로 남음
- 병합 방법 3가지를 적절히 사용하면, 위에서 언급한 아쉬움을 최소화 할 수 있을 것
