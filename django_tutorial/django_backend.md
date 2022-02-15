## công nghệ sử dụng 
- python https://www.codecademy.com/catalog/language/python
- django https://docs.djangoproject.com/en/4.0/ 
- restapi  https://www.django-rest-framework.org/tutorial/1-serialization/
- docker https://docs.docker.com/get-started/
- celery https://docs.celeryproject.org/en/stable/
- postgresql https://www.postgresql.org/docs/


## TẠO ENV 
Sử dụng conda
https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html
theo cách thông thường 
https://docs.python.org/3/library/venv.html
- tạo project sử dụng django-admin strat project 

### Một số lệnh trong manage.py 
- startproject tạo project 
- shell chạy thử lệnh 
- startapp tạo app 
- runserver chạy dự án 
- makemigrations tạo ra file mô tả, lưu lại lịch sử thay đổi trên cơ sở dữ liệu 
- migrate thực thi những lệnh do makemigrations tạo ra rồi apply nó vào trong database thật 
-

### Tổ chức thư mục 

1. Gợi ý 
- https://github.com/sonnhfit/django_base
- https://github.com/saleor/saleor
- https://github.com/MicroPyramid/Django-CRM

2. default 
```
mysite/
    manage.py
    mysite/
        __init__.py
        settings.py
        urls.py
        asgi.py
        wsgi.py
polls/
    __init__.py
    admin.py
    apps.py
    migrations/
        __init__.py
    models.py
    tests.py
    views.py
```

4.

5. unit test https://pytest-django.readthedocs.io/en/latest/

#### lưu trữ media 
- https://boto3.amazonaws.com/v1/documentation/api/latest/index.html


### docker service 
- nginx webserver, proxy, cân bằng tải
- redis cơ sở dữ liệu trên ram cache. OTP tồn tại 60s sử dụng redis 
- db: 
    - backup + restore https://github.com/sonnhfit/mynote/blob/master/load_sql_docker.MD

- celery: lập lịch, bất đồng bộ, task chạy ẩn 


Trong docker mỗi service thì là một cái container có thể nói một cách dễ  hiểu là một cái máy ảo, mình phải cài rất nhiều thứ linh tinh ví dụ phần mềm, thư viện, env, ... nó định nghĩa trong file `docker-compose.yaml` và file `Dockerfile`



