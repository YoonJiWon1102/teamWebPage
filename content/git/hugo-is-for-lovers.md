+++
title = "Hugo is for lovers"
date = "2015-08-03T13:39:46+02:00"
tags = ["hugo"]
categories = ["pseudo"]
banner = "img/banners/banner-3.jpg"
summary="This is the summary Goto [hugo releases](https://github.com/spf13/hugo/releases) and download the appropriate version for your os and architecture. Save it somewhere specific as we will be using it in the next step. More complete instructions are available at [installing hugo](/overview/installing/)"
+++

## What is branch? 
다른 작업에 영향을 받지 않고 독립적으로 작업을 하기 위한 개념.
여러 작업을 동시에 하기 편함.


## How to create a branch?

Creating a new branch in remote:

 1. 깃허브에서 브랜치 만들기
 2. git fetch -p
 3. git checkout <브랜치 이름>
 
Creating a new branch in local:

 1. git branch <브랜치 이름>
 2. git checkout <브랜치 이름>
 3. git push <원격><브랜치 이름>
 4. git branch -a
 
## How to merge branch?

merge order:
 
 1. 로컬에서 수정한 작업을 원격으로 푸시
    a. git add .
    b. git commit -m “수정메세지”
    c. git push

 2. 원격 저장소로 푸시되고 나면 병합 작업
    a. PR 생성 후 검토
    b. merge

 3. 로컬 저장소 동기화 및 브랜치삭제
    a. git checkout main
    b. git pull
    c. git branch -d <삭제할 브랜치 이름>
    d. git push orgin —delete <삭제할 브랜치 이름>

## branch command

git branch # 현재 브랜치 확인하기
git branch name1 # name1이라는 브랜치 새로 만들기 
git checkout name1 # name1 브랜치로 체크아웃(이동하기)
git branch -a # 모든 branch 정보를 보여줍니다.
git log --oneline # 한 줄에 한 커밋씩 나타내줌, 커밋을 확인할 때 유용
git log --oneline --branches # 각 브랜치의 최신 커밋을 볼 수 있음
git branch -d name1 # 로컬에서 name1 브랜치 삭제하기
git push origin --delete name1 # 원격에 있는 name1 브랜치 삭제하기



