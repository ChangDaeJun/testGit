# testGit
git실험실


### This commit does not belong to any branch on this repository, and may belong to a fork outside of the repository. 구현

1. 새로운 브런치를 생성한다.(여기서는 new로 생성)
2. 새로운 브런치에 새로운 커밋을 생성한다.(null 커밋 생성)
3. 브런치를 삭제한다.
4. https://github.com/ChangDaeJun/testGit/commit/0252f3648de96388d9df62b4cf68058330f63894 와 같이 어떠한 브렌치에도 속하지 않는 커밋이 생성된다.

* 이유 : 브랜치는 특정 커밋을 가리키는 포인터의 역할이다. 중요한 정보는 커밋이 스냅샷 단위로 관리하게 된다. 따라서 브랜치를 삭제한다는 것은 커밋을 삭제하는 의미가 아니기에, 브렌치를 삭제해도 커밋은 계속 남게 된다.

