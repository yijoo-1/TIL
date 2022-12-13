# TIL Day 02
>2022 12월 13일

## **CLI 기초**
---
### GUI vs CLI
1. GUI(Graphic User Interface): 그래픽을 통해 사용자오 상호작용하는 방식
2. CLI(Command Line Interface): 터미널을 통해 사용자와 컴퓨터가 상호작용하는 방식

**why Git Bash?**
- 명령어의 통일을 위해서

### 경로
1. 루트, 홈 디렉토리
- 루트 디렉토리 
- 홈 디렉토리

2. 절대경로와 상대경로
- 절대경로 : C:/Users/kyle/Desktop
- 상대 경로 : ./ 현재 작업하고 있는 폴더 의미

### 터미널 명령어
1. touch
- 띄어쓰기로 구분하여 여러 파일을 한꺼번에 생성 가능
- 숨김 파일 : .
2. mkdir
- 띄어쓰기로 여러 폴더 한꺼번에 생성 가능
- 폴더 이름에 공백넣기 : ''
3. ls
- -a : all옵션
- -ㅣ : long옵션
4. mv
- 폴더/파일을 다른 폴더내로 이동하거나 이름을 변경하는 명령어
5. cd
- cd (~) : 홈 디렉토리로 이동
- cd .. : 부모 디렉토리
- cd - : 바로 전 디렉토리(뒤로가기)
6. rm
- 폴더/파일 지우는 명령어
- _*_ : 파일 전체 지움
- -r 
7. start, open
- 폴더/파일 여는 명령어

### 유용한 단축키
- 위아래 방향키: 과거 작성한 명령어 조회
- tab : 폴더/파일 이름 자동완성
- ctral+a(커서맨앞)<-->ctrl+e(커서맨뒤)
- ctrl+l: 화면 청소(땡기기)
- clear : 모두 지움
-  ctrl+w: 커서가 앞단어 삭제
-  ctrl+insert/shift+insert:  복사/붙여넣기

## **Markdown**
---
### 문법
1. 제목
- #~######
2. 목록
- 순서없는 목록: - * +
- 순서있는 목록: 1. 2. 3.
- tab 키 : 들여쓰기
3. 강조
- 취소: ~~글자 ~~
- 기울임: `*글자*` `_글자_`
- 굵기: `**글자**` `__글자__`
4. 코드
- 인라인코드 :`inline  code`
- 블록코드 : ```python``` 
5. 링크 : `[]()`
6. 이미지 :`![]()`
7. 인용: > 갯수에 따라 중첩 가능
8. 표 : 
9. 수평선 : -*_ 3번 이상 연속 작성

## **Git 기초**
***
### 초기설정
>최초 한 번만 설정
1. 누가 커밋 기록을 남겼는지 확인할 수 있도록 이름,이메일 설정
```
git config --global user.name "이름"
git config --global user.email "메일 주소"
```
2. 올바르게 설정되었는지 확인
```
git config --global --list
```

## **Git 기본 명령어**
---
>Working Directory(working tree)->Staging Area(=index) -> Repository
1. git init 
    - 현재 작업 중인 디렉토리를 git으로 관리한다는 명령어
    - 터미널에(master)표기
    - 주의: 중복 설정x / 홈 디렉토리에서 git init x
2. git status
    - working directory와 staring area에 있는 파일 현재 상태 알려주는 명령어
    - untracked
    - tracked: unmodified/ modified/ staged
3. git add
    - working directory에 있는 파일을 sraging area로 올리는 명령어
    - untracked, modified-->staged
4. git commit
    - staging area에 올라온 파의 변경사항을 하나의 버전(커밋)으로 저장하는 명령어
5. git log
    - 커밋의 내역(id, 작성자, 시간, 메세지 등) 조회 명령어
    - 옵션 : --oneline --all --graph --reverse -p -2
6. git remote
   - 로컬저장소에 원격저장소를 등록, 조회, 삭제 할 수 있는 명령어
   - git remote add <저장소이름><주소>
   - git remote -v
   - git remote rm <저장소이름>
7. git push
   - 로컬저장소의 커밋을 원격저장소에 업로드하는 명령어
   - git push -u <저장소이름><브랜치이름>
   - 주의! github 원격저장소에 저래돌 파일을 드래그해서 업로드x
