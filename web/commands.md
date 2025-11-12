venv 생성
- python -m venv (venv name)

ipython: 편리한 파이썬 작업환경을 만들어주는 도구
- pip install ipython

django shell 접속
- python manage.py shell


user model 참조할때

import django.conf import settings
settings.AUTH_USER_MODEL
---
django.contrib.auth import get_user_model
User = get_user_model()