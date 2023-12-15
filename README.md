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
    add 명령: 작업공간 >> 스테이징 역역
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
  cat(Concatenate) 파일 내용 화면 출력<br>
  Redirection 명령어 ( >, >>) 화면의 출력 결과를 파일로 저장<br>
> $rm -rf.git 전체 폴더를 삭제& 하부 폴더 git 삭제

   



      



***
## 깃허브 이용시 도움 되는 자료
[깃허브 기초](https://www.youtube.com/watch?v=Z9dvM7qgN9s)


[깃허브 1시간안에 끝내기](https://xn--youtube-h503a.com/watch?v=-27WScuoKQs)
