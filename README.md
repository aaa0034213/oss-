# oss

2023 2학기 오픈소스소프트웨어
---

## 1주차 oss 정리
> 1주차 oss <br>
  - 버전 관리: 파일 집합에 대한 변경사항 추척,관리<br>
  - 커밋 버전 관리: 저장소 현 상태에 저장하는 행위, 파일 집합의 변경 내용 >> 깃 저장소(Git repository) 에 기록<br>
1. **커밋과 버전관리**<br>


   커밋(commit): 저장소 현 상태에 저장하는 행위<br>
   HEAD: 가장 최근의 커밋을 가리키는 포인터<br>

   
2. **원격 저장소와 지역 저장소 명령**<br>


  >  Clone: 서버의 원격 저장소를 지역 저장소에 복제<br>
    Push: 서버 원격 저장소로 올리기<br>
    Pull: 지역 저장소로 내리기 <br>
    add,commit : 파일을 저장소에 저장하는 명령어<br>

    
3. **버전 관리 시스템**<br>


>    종류: CVS,SVN,GIT,Mercurial,Bazarr
<br>

4. **깃과 깃허브**<br>
  > 깃: 컴퓨터 파일의 추적하는데 사용되는 버전 관리 시스템<br>
    깃 내부: 작업 디렉토리, 작업공간, 스테이징 영역, 깃 저장소, 임시 저장소<br>
    add 명령: 작업공간 >> 스테이징 영역
    commit 명령: 스테이징 영역 >> 깃 저장소<br>

---
## 2주차 정리
>2주차 oss<br>
1. **깃 설정 & 저장소 생성**<br>


   $git config -- 설정범위 설정변수<br>
   --system, --global, --local<br>

   core.editor['code--wait] #기본 편집기 설정<br>
   --global --edit #전역 설정 파일 편집<br>
   core.autocrlf true # 줄바꿈 자동전환 <br>
   core.selfcrlf false # 줄바꿈 안전설정<br>
   $git init # 저장소 생성<br>

2. **vscode 리눅스 명령**<br>
> 중요한 것<br>
  touch fname 빈 파일 fname 생성<br>
  cat(Concatenate) 파일 내용 화면 출력<br>
  Redirection 명령어 ( >, >>) 화면의 출력 결과를 파일로 저장<br>
   $rm -rf.git 전체 폴더를 삭제& 하부 폴더 git 삭제<br>
---
## 3주차 oss
>3주차 oss<br>

  1.**깃 커밋**<br>

  > 깃 영역: 작업 디렉토리, 스테이징 영역, 깃 저장소<br>
    add 명령: 작업공간 >> 스테이징 영역
    commit 명령: 스테이징 영역 >> 깃 저장소<br>

  2. **버전 로그 이력**<br>

  > $git log 로그 이력 정보 표시<br>
    $git log --oneline 로그 이력 한 줄 표시<br>
    $git log -p 로그 이력&파일 변화 표시<br>
    $git show 마지막 커밋(HEAD) 커밋 정보 표시<br>

  3. **로그 이력 과거 여행**<br>

  >  과거 커밋 HEAD~ 이동 (check)<br>
      $git checkout HEAD~  HEAD 이전 커밋 이동<br>
      $git chechkout-    이전 checkout 이동<br>
      $git checkout main  브랜치 마지막 커밋 이동<br>

  > 과거 커밋 이동 (switch)<br>
      $git switch -d 이전커밋<br>
      $git switch [branch]<br>
      $git swithch -c [newbranch]  새로운 브랜치 생성후 이동<br>
---

## 4주차 oss
>4주차 oss<br>

  1. **파일 비교 diff**<br>

    >작업 드렉토리  스테이징 영역  깃 저장소
     작<스 ($git diff) / 스<깃 ($git --staged HEAD) / 작<깃 ($git diff HEAD)

    커밋 간의 파일 비교시
    $git diff [비교파일1][비교파일2]
    $git diff 000abc 111dfg<br>

    
  2. **파일 삭제 rm**<br>

    리녹스 명령 파일삭제
    > $rm [file]  작업 디렉토리에서 file 삭제.
      $git rm [file]  작업 디렉토리, 스테이징 영역 file 모두 삭제
      $git rm -catched [file]  스테이징 영역 file 삭제

  3. **파일 복원 restore**<br>

      파일 복원
     > $git restore [file]  작업 디렉토리 파일 스테이징 영역 파일로 복구<br>
       $git restore --staged [file] 깃 저장소 최신 커밋 상태 스테이징 영역 복구<br>
       $git restore --source=HEAD--staged--worktree f 현재 내용으로 작업,스테이징 영역 모드 같은 상태 복구<br>
---

##5주차 oss
>5주차 oss<br>

  1. **버전과 태그**<br>

  +버전(version): 프로그램 수정,코드를 구분 식별자 (숫자 사용, 년월 사용)<br>
    -major,minor,patch (메이저 번호, 마이너 번호, 패치 반호)

  + 태그(tag): 특정 커밋 버전 번호나 다른 이름 부여하는 기능
    주석 태그, 일반 태그 use<br>

    주석태그: 주석이 있는 태그, 태그 버전 이름 중복 x<br>
    >$git tag : 예전 태그부터 표시<br>
    $git log : 최신 커밋부터 표시<br>
    $git tag- a v1.0.0 -m '메세지 정보' / 이메일, 날짜, 메세지 등 정보를 포함함<br>
    $git tag -a v.1.0.0 / 기본 설정된 편집기 실행 <br>
    $git tag -d (태그 삭제)<br>


  2. **브랜치 개요 관리**<br>

  + 브랜치 (branch) 버전을 다양하게 작업 할 수 있게 하는 기능 / 커밋 사이를 가볍게 이동하는 포인터<br>
    -HEAD: 작업중인 브랜치 최신 커밋 가르키는 포인터 (checkout, switch ) 가능<br>

     브랜치 생성<br>
      >$git branch bname  단순히 생성, HEAD 이동 x<br>
      $git switch -c bname or checkout -b name  //생성 후 새 브랜치 HEAD 이동 o<br>
      $git switch [bame] / checkout [bname]  // HEAD 지정한 브랜치로 이동<br>
      $git switch - / checkout -  // 이전 브랜치로 이동<br>
      $git branch -d branch -name   // 저장소 삭제<br>


    ---

  ## 6주차 oss
  > 6주차 oss<br>

  1.**원격 저장소 복제**<br>

    +원격 저장소 생성 >> 복제 (Clone)

  > $git clone [복사주소]    원격저장소 동일한 이름 복제<br>
    $git clone [복사주소][새로운 폴더]    하루 폴더 새로운 폴더 명으로 복제<br>
    $git remote   원격 저장소 이름 목록만<br>
    $git remote -v 원격 저정서 주소 이름 목록<br>

   2. **유명 OSS**<br>

   +유명 OSS

  1. vscode 2. atom 3. VCS 깃 4. 구글 인공지능라이브

  3. **지역과 원격 저장소 연동 Push Pull**<br>

  > Push : 지역 저장소에서 원격 저장소로<br>
    Pull : 원격 저장소에서 수정 후 지역 저장소로<br>

    $git pull = git fetch + git merge 
    (1) fetch : 원격 저장소에서 로컬 저장소로 소스 가져와 병합 미수행 명령
    명령어: $git fetch <remote>
    (2) merge : 깃 허브 내용 반영하려면 필요한 과정 (병합)

    $git push : 지역 저장소 수정 사항을 push 로 원격 저장소로 보내는 명령

---
## 7주차 oss
>7주차 oss<br>

1.**OSS**<br>

>(1) OSS (open source software ) : 누구나 제약없이 코드 보고 사용할 수 있는 오픈 소스 라이선스 SW<br>
의미: 소프트웨어 소스코드 자유롭게 읽고 수정 재배포 가능<br>
(2) OSS 장단점: 소스코드 공개, 커스터마이징, 혁신 지원 / 단점: 공개 의무 품질 보증 및 유지보수 보안 등 어려움<br>
(3) 다양한 OSS: Python, Scikit-learn, Tensorflow, Pytorch<br>
(4) 대표 라이선스
>
|라이선스|배포 시 라이선스 사본 첨부|저작권 고지 사항유지||소스코드 제공 의무 범위|타 라이센스 통합 배포 가능|수정 시 수정 내용 공지|
|------|---|---|---|---|---|---|
|GPL 2.0|o|o||전체 코드|조건부|x|
|GPL 3.0|o|o||전체 코드|x|o|
|LGPL 3.0|o|o||전체 코드|o|o|
|BSD|x|o||x|조건부|x|
|Apache2.0|o|o||x|o|x|

(5) 의무 강도 : GPL>LGPL>BSD>MIT ( > 강도 높은 쪽 )<br>

2. **Stash**<br>

 stash 필요성: 브랜치 이동 or 이전 커밋 이동하기 위해<br>

>(1) $git stash  작업 디렉토리 스테이징 영역 stash 저장 작업 폴더 정리<br>
  옵션: --keep-index 스테이징 영역 제외 작업 폴더만 저장 // --include-untracked  untracked 포함해 저장<br>

  (2) $git stash apply  작업 디렉토리 내용만 복사해 활용<br>
  $git stash apply --index  스테이지 영억도 함께 복사<br>

  (3) Stash 목록보기<br>
    $git stash list <br>

    
  (4)특정 stash 확인<br>
    $git stash show<br>

3. **pop & drop**<br>

    > $git stash pop / pop stash@{n}  최근 지정된 임시저장소 내용 가져와 반영하고 삭제<br>
      $git stash drop  최근 임시저장 내용 삭제<br>
      $git stash drop stash@{n}  지정된 임시저장 삭제<br>
      $git stash clear  모든 stash 목록 제거<br>
      $git clean    Untracked 파일 삭제 >> 바로 삭제 x <br>
      >> $git clean-i  삭제하고 싶은 파일 삭제 가능 //  $git clean-f  무조건 삭제하는 기능.<br>


---
## 8주차 oss
>8주차 oss<br>

  1.**브랜치 병합 개요**<br>

  (1) 병합(merge): 두 개 브랜치를 하나로 모으는 과정<br>
  > fast-forward, 3-way 병합 <br>

    fast-forward 조건: 현재 브랜치 master 가 병합 대상 커밋의 직접 뿌리인 경우
    master 단순히 이동 작업공간, 스테이징 영역 이동
    병합할 브랜치 조상 기준 브랜치인 경우 (일렬 상태) fast forward 사용
    >> $git merge bugfix

    3-way 조건: 두 브랜치 조상이 같은 경우 가능
    새로운 커밋을 사용하여 두 기록을 합침
    >> $git merge  bugfix
  
  (2) 두 브랜치 일렬 상태 2가지 병합
      옵션 x = (fast-forward merge) $git merge topic // 옵션 --no--ff = (3-way merge) $git merge --no--ff topic

  (3) 병합 다양한 옵션<br>
      $git merge --ff-only {병합할 브랜치 명}  상태 fast 인 일렬 상태에서만 병합 o
      $git merge --squash {병합할 브랜치 명}  현재 브랜치에 병합 대상과 합치는 커밋 하나 생성후 병합

    * squash : 강압적 병합<br>

2.**병합 충돌과 해결**<br>

>(1) 파일 충돌 발생시 : 병합한 두 브랜치 마지막 커밋 비교 // 두 브랜치 모두 변경 사항 달리 발생한 파일 수정.<br>
 (2) 충돌 파일 vscode 확인: **<<<<<<<** 색상<br>
 (3) 충돌 해결 방법: 1. 병합 취소: $git merge --abort // 다시 병합 $git merge feat/list<br>
 이후 추가,커밋 다시 >> $git commit -am 'Resolve confilct,main'<br>

 ---

 ## 9주차 oss
 >9주차 oss<br>

1.**rebase**<br>

  >(1)rebase  선형으로 단순하고 깨끗한 이력 사용, 원래 커밋 이력 변경 (정확한 커밋 이력시 사용 x)<br>
  *두 갈래 브랜치에서 기존의 베이스를 수정 >> 병합할 브랜치 마지막 커밋 새로운 베이스로 수정 병합<br>

  (2)일반적 rebase 방법: topic 에서 main rebase 이후 다시 main 이동 fast-forward 병합수행<br>
    $git checkout topic >> $git rebase main >> $git checkout main >> $git merge topic<br>

  (3)다른 rebase 방법: main topic 순서로 재배치 방법<br>
    $git rebase main topic >>  $git checkout main >> $git merge topic<br>
    
2.**커밋 이력 수정**<br>


  >(1) 최근 커밋 내용 수정: $git commit --amend' // 기본 편집기로 메세지 입력<br>
    $git commit --amend -m 'new message'// 기본 편집기 메시지 입력<br>
    $git commmit --amend --noedit  // 수정 x  다시 커밋 수정<br>


    (2) 이전 커밋 HEAD~2, HEAD~, HEAD 각각의 커밋 수정<br>
    $git rebase --interactive HEAD~3<br>

    (3) rebase-i 명령어 : pick 해당 커밋 수정 x 그대로 use, reword 개별 커밋 메세지 다시 작성, squash 계속된 이후 커밋을 이전 커밋에 결합, drop 커밋 자체 삭제<br>

    
---

## 10주차 oss
>10주차 oss<br>

  1.**reset**<br>

  reset  커밋 이력에 이전 특정 커밋으로 완전히 되돌아가는 방법<br>
  (1) reset 옵션: --hard, --mixed, --soft // 무조건 깃 저장소에는 복사됨

  > 옵션 hard  (HEAD~)  지정된(HEAD~) 내용으로 작업 폴더 스테이징 영역, 깃 저장소 모두 복사 수정, reset 전 작업 폴더, 스테이지 영역 작업 내용 모두 사라짐.<br>

  mixed  (HEAD~2)  지정된(HEAD~) 내용으로 스테이지 영역과 깃 저장소에 모두 복사 수정, reset 전 커밋 메세지 로그이력과 스테이지 영역, 깃 저장소 내용 모두 사라짐. //  작업 폴더 내용 이전 그대로<br>

  soft  (HEAD~) 지정된(HEAD~)  내용으로 깃 저장소에만 복사 수정, 커밋 메세지 로그 이력 사라짐. // 작업 폴더, 스테이지 영역 내용 모두 이전 그대로 남음<br>

  hard  >> 파일 수정 , add , commit 필요 , mixed >>  add , commit 필요 , soft >>  commit 필요<br>

  (2) reset 이후 다시 바로 이전 상태로 되돌아가기<br>
  $git reset --hard ORIG_HEAD<br>
    


      
    
       
      
    

      
    



      



***
## 깃허브 이용시 도움 되는 자료
[깃허브 기초](https://www.youtube.com/watch?v=Z9dvM7qgN9s)


[깃허브 1시간안에 끝내기](https://xn--youtube-h503a.com/watch?v=-27WScuoKQs)
