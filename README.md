==============
# CardDrawGame
==============

Overview
==============
Web Server 와 HTML을 활용하여 카드뽑기게임을 만든다. (프로그래밍 언어나 환경은 자유)

Requirements
==============
- Python 2.7

Install
==============
    $ virtualenv venv
    $ source venv/bin/activate
    $ pip install Flask
    $ brew install mongodb
    $ pip install pymongo==2.8
    $ pip install Flask-MongoKit

How To Run
==============
MongoDB Server를 올리기 위해 최상위 디렉토리에서 폴더를 만들고, MongoDB Server를 올린다.

     $ sudo mkdir data
     $ sudo mkdir data/db
     $ mongod
     $ python manage.py runserver


How To Play
==============

카드
   - 카드에는 S, A, B, C, D 의 급이 있다.
   - 카드별로 뽑힐 확률이 다르며, S급이 가장 뽑기 어렵고 D급이 가장 뽑기 쉽다.
   - 카드별로 공격력이 다르며, S급이 가장 강력하고 D급이 가장 약하다. (공격력은 integer 이다.)


페이지 구성

  카드보기 페이지:
   1. 현재 가지고 있는 카드를 보여준다.
   2. 카드의 급, 갯수, 합산 공격력을 보여준다.
   3. 새로운 카드를 뽑기위해, 뽑기 페이지로 넘어갈 수 있다.

뽑기 페이지
   1. 새로운 카드를 뽑을 수 있다.
   2. 카드를 뽑으면 뽑은 결과를 보여준다.
   3. 카드를 뽑은 뒤에 다시 새로운 카드를 뽑거나, 카드보기 페이지로 넘어갈 수 있다.



추가점수 요소

1. 합성기능, 낮은 급의 카드 2장을 합성하여 상위 급의 카드 1장을 만들 수 있다.
       ex) C급 카드 2장을 합성하여 B급 카드 1장을 만듬
2. 카드 버리기 기능, 카드를 버릴 수 있음
       ex) A 카드 2장 보유시, 1장를 버리고 1장이 됨
 
