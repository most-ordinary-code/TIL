# 원격 저장소 (Remote Repository)

## 기본 설정

1. 로컬 git 저장소 준비
2. Github repository 생성
3. Repository default branch 변경 (settings → repositories)
   - main → master로 변경

<br>

## 명령어

### 원격 저장소 주소 추가

```bash
$ git remote add origin "저장소 url"
```

> "git아, 원격 저장소(remote) 추가(add)해줘, origin 이라는 이름으로 저장소 url을!!!"

- origin은 원격 저장소 이름!

<br>

### 원격 저장소 목록 보기

```bash
$ git remote -v
origin  https://github.com/seongwoolim-dev/TIL.git (fetch)
origin  https://github.com/seongwoolim-dev/TIL.git (push)
```

> 잘못 add한 경우, 삭제하기
>
> ```bash
> $ git remote rm origin
> ```

<br>

### 원격 저장소에 업로드 (push)

```ba
$ git push -u origin master

Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 75.02 KiB | 7.50 MiB/s, done.
Total 6 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/seongwoolim-dev/TIL.git
 * [new branch]      master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.
```

> "git아, push 해줘 origin이라는 이름의 원격 저장소에 master 브랜치로!!!"

> **원격 저장소에는 commit이 올라간다!**
>
> *즉, commit 이력이 없다면 push 할 수 없다.*

> 주의: github 내에서는 절대 수정 하지 말 것, **로컬**에서 수정!!!

<br>

### pull

- 원격 저장소의 변경 사항을 받아옴 (업데이트) 

```bash
$ git pull origin master
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 673 bytes | 32.00 KiB/s, done.
From https://github.com/seongwoolim-dev/TIL
 * branch            master     -> FETCH_HEAD
   8bb4986..859c63a  master     -> origin/master
Updating 8bb4986..859c63a
Fast-forward
 README.MD | 3 ++-
 1 file changed, 2 insertions(+), 1 deletion(-)

```

<br>

### clone

- 원격 저장소 전체를 복제

```bash
$ git clone "저장소 url"
```

> [주의사항]
>
> clone 받은 프로젝트는 이미 `git init`이 되어있음. (`remote` 도 추가되어 있음)

---

