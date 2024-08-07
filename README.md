# Django-project-setup-Installation

1. python -m venv .venv
 1a. .venv\Scripts\activate 
2. django-admin startproject myapp
 2a. cd myapp
3. pip install django
4. python manage.py startapp demo
5. pip install djangorestframework
6. pip install mysqlclient
7. pip install django-cors-headers
8. python manage.py runserver
9. python manage.py makemigrations
10.python manage.py migrate

setting.py:

//app
    INSTALLED_APPS = [
    'demo',
    'corsheaders',
    'rest_framework',
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
]

//middleware
MIDDLEWARE = [
    'django.middleware.security.SecurityMiddleware',
    'django.contrib.sessions.middleware.SessionMiddleware',
    'django.middleware.common.CommonMiddleware',
    'django.middleware.csrf.CsrfViewMiddleware',
    'django.contrib.auth.middleware.AuthenticationMiddleware',
    'django.contrib.messages.middleware.MessageMiddleware',
    'django.middleware.clickjacking.XFrameOptionsMiddleware',
    //corsheaders
    'corsheaders.middleware.CorsMiddleware',
    'django.middleware.common.CommonMiddleware',
]

//database
DATABASES = {
    'default': {
         'ENGINE': 'django.db.backends.mysql',
        'NAME': 'DB_img_demo',
        'USER': 'root',
        'PASSWORD': 'admin',
        'HOST': 'localhost',
        'PORT': '3306'
    }
}
//cors origin
CORS_ALLOW_ALL_ORIGINS = True

CORS_ALLOW_CREDENTIALS = True  # Allow cookies to be included in CORS requests

CORS_ALLOW_HEADERS = [
    'content-type',
    'authorization',
    'x-requested-with',
    'accept',
    'origin',
    'x-csrftoken',
]
