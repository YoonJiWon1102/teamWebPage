+++
title = "Linked post"
date = "2015-10-02T21:49:20+02:00"
tags = ["golang", "programming", "theme", "hugo"]
categories = ["programming"]
banner = "img/banners/banner-4.jpg"
authors = ["John Doe","Jane Doe"]
+++

## 깃허브로 협업하기

1. 원격 저장소 복제하기 
    
    git clone <github-url> : 원격 저장소를 로컬로 가져오는 명령어
    
2. 로컬에서 작업하고 깃허브에 올리기 
    
    git commit -am “메세지” (-am 옵션: add 까지 한꺼번에 함)
    
    git push
    
3. 원격저장소 커밋을 로컬로 가져오기
    
    git pull
    
    ### Git hub project step
    
    1. 깃허브에서 브랜치 만들기
    2. git clone <github-url> 
    3. 서브모듈 업데이트
    4. 원격에서 만든 브랜치 로컬로 가져오기
        1. git fetch -p
        2. git chekcout <브랜치이름>
        3. git branch -a : 브랜치 확인
    5. 작업 수정
        1. 새로 만든 브랜치에서 수정
    6. 빌드 및 푸시
        1. 깃허브에서 협업할 때는 먼저 git pull를 해서 원격저장소의 최신 커밋을 풀한 뒤에 자신의 커밋을 push하기
        2. ![rejected] 오류 메세지: 원격 저장소에 있는 최신 커밋 정보가 없기 때문에 나타나는 메세지 
    7. 브랜치 병합
        1. PR 생성 후 검토
        2. 병합
    8. 로컬 저장소 동기화
        1. git checkout main
        2. git pull
    9. 브랜치 삭제
        1. git branch -d <삭제할 브랜치 이름>
        2. git push orgin —delete <삭제할 브랜치 이름>