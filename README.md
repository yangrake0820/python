# python 게시판 프로젝트

# Chapter.1

1) 가상환경 구성
    python -m venv venv 

2) 가상환경 접근
    venv\Scripts\activate

3) 장고 설치
    pip install django

4) 프로젝트 시작
    django-admin startproject config .

5) app 생성
    python manage.py startapp accounts
    python manage.py startapp boards

6) app 등록
    config > settings.py > INSTALLED_APPS[] 에 추가

7) accounts/models.py 모델 생성

8) accounts 모델 적용
    python manage.py makemigrations accounts
    python manage.py migrate accounts
    python manage.py migrate

9) 관리자 계정 생성 및 어드민 페이지 등록
    python manage.py createsuperuser
    accounts/admin.py 들어가서 모델과 연결

10) 확인
    python manage.py runserver

    http://127.0.0.1:8000/      기본 메인 페이지
    http://127.0.0.1:8000/admin 관리자 페이지

# Chapter.2
1) accounts html 생성 
    templates 폴더 안에 위치 하도록

2) 부트스트랩 적용 및 static 폴더 생성 및 추가
    static 폴더 생성 : 루트에 위치 하도록
    config > settings.py 

        import os

        STATICFILES_DIRS = [
            os.path.join(BASE_DIR, 'static'),
        ]

3) url 연결 
    1. config > urls.py 에서 app 별로 include 해주기
    2. accounts > urls.py 
    3. accounts > views.py
