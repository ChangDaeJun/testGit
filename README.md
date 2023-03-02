# testGit
git실험실


## This commit does not belong to any branch on this repository, and may belong to a fork outside of the repository. 구현

### 브렌치 삭제로 인한 생성

1. 새로운 브런치를 생성한다.(여기서는 new로 생성)
2. 새로운 브런치에 새로운 커밋을 생성한다.(null 커밋 생성)
3. 브런치를 삭제한다.
4. https://github.com/ChangDaeJun/testGit/commit/0252f3648de96388d9df62b4cf68058330f63894 와 같이 어떠한 브렌치에도 속하지 않는 커밋이 생성된다.

* 이유 : 브랜치는 특정 커밋을 가리키는 포인터의 역할이다. 중요한 정보는 커밋이 스냅샷 단위로 관리하게 된다. 따라서 브랜치를 삭제한다는 것은 커밋을 삭제하는 의미가 아니기에, 브렌치를 삭제해도 커밋은 계속 남게 된다.


### 원격 저장소의 커밋 삭제

특히, 원격 저장소의 커밋을 삭제하는 방법도 해당 문제를 발생시킨다.

해당 방법은 보통 로컬 저장소에서 해당 커밋을 지운 뒤 원격 저장소로 강제 푸쉬를 하는 방법으로 이루어진다. 하지만, 커밋은 git 저장의 단위이기에 위와 같은 방식으로는 삭제되지 않는다.

1. 삭제될 커밋을 원격 저장소에 올림
![스크린샷 2023-03-02 오후 5 08 31](https://user-images.githubusercontent.com/97227920/222371117-9ce469e2-350e-4a8b-bf6e-07691dfe42fe.png)

2. 해당 커밋을 삭제함.
![스크린샷 2023-03-02 오후 5 15 46](https://user-images.githubusercontent.com/97227920/222371234-d62b7386-1e73-4e05-88a9-93d5f635e200.png)

3. 해당 커밋의 링크는 여전히 존재한다. : https://github.com/ChangDaeJun/testGit/commit/faffd3f56623f602f9925ff973c5c62789006ab8
