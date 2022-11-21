# 개요
- 레이블은 Issue 또는 Pull Request작업에서 카테고리를 분류하는 이름표같은 개념이다.
- 기본으로 9개의 레이블을 제공한다.
![image](https://user-images.githubusercontent.com/113485036/202969398-397436fc-a21d-491b-aa84-03b73e6f6ed2.png)

# 레이블 추가
- 레이블 편집창에서 New Label을 클릭한다.
- 제시된 양식을 전부 기재하고, Create Label 버튼을 클릭한다.
![image](https://user-images.githubusercontent.com/113485036/202969948-ad604984-abe0-4214-8a28-de67e4bf90c8.png)

# 이슈 및 PR에 레이블 적용
- 이슈 및 PR 세부사항에 들어가서 우측 Labels의 톱니바퀴를 클릭하여 Label을 추가할 수 있다.
- 이슈에서는 다음과 같다.
![image](https://user-images.githubusercontent.com/113485036/202970184-320a3faa-ebaf-4f90-a862-f7534405879c.png)
- Pull Request에서는 다음과 같다.
![image](https://user-images.githubusercontent.com/113485036/202970115-f6c7d19d-483b-4384-aabe-62aaf6f69c62.png)

# 레이블을 한꺼번에 생성하기
- 위에서 언급한 레이블 추가 방법을 이용해서 레이블을 추가하면, 한번에 하나씩밖에 생성이 안된다.
- 한꺼번에 많은 레이블이 필요할 경우에는 이는 매우 비효율적인 방법이다.
- 이때문에 lables.json이라는 파일을 준비하여, personal access token을 활용하여 github에 올리는 과정을 거친다.
- 먼저 lables.json을 생성한다.
![image](https://user-images.githubusercontent.com/113485036/202974191-e63dba4f-794b-4ea6-991c-966925e38a48.png)
- 그 후 git personal access token을 생성하고 Local PC에서 npx를 활용하여 github repository에 업데이트한다.
![image](https://user-images.githubusercontent.com/113485036/202976013-18d45602-a245-4261-b4cf-0bfa173b7965.png)
- 지정된 저장소에 가서 label의 업데이트 여부를 확인한다.
![image](https://user-images.githubusercontent.com/113485036/202976103-643342b1-886a-4ede-94e0-42a39ae4f20e.png)

# 사용 평가
- 레이블을 통해 카테고리를 분류할 수 있는 점은, 이슈나 PR이 카테고리 별로 필터링되므로 가독성이 높아짐
- 레이블 등록 기능은 한번에 하나의 레이블밖에 등록이 안되므로 이로 인해 생기는 불편함을 어느정도 감수해야 함
- json파일을 생성 후, 한꺼번에 레이블을 업로드하는 방식으로 이를 해결할 수 있다는 것을 알게 되면 편리하게 사용할 수 있는 기능이라고 생각함
