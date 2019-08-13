Bật termial ở máy rồi thực hiện các bước sau
### 1. Tạo 1 thư mục mới bằng lệnh sau 
```
mkdir tenthumuc  
```
trong đó ```tenthumuc``` la tên thư mục của bạn 

### 2. di chuyển thư mục làm việc working dir vào trong thư mục vừa tạo 

```
cd tenthumuc 
```

### 3. tạo virtual env với pyenv lưu ý cần cài đặt pyenv và sử dụng pyenv để install python 3.6.6 trước 

```
pyenv virtualenv 3.6.6 newenv 

```
### 4. active env bằng lệnh sau 
``` pyenv local newenv ```

### 5. cài đặt django bằng lệnh 

``` pip install django ```

### 6. tạo project django mới bằng lệnh sau 

``` django-admin startproject yourproject .
```
lưu ý là lệnh trên có đáu "." 

### 7. tạo 1 file 
``` docker-compose.yml ```
với nội dung như sau 


```shell 
version: '3.6'

services:
  db:
    image: postgres:10
    ports:
      - "5432:5432"
    environment:
      POSTGRES_PASSWORD: rootapp123
    volumes:
      - postgres_data:/var/lib/postgresql/data/
  redis:
    image: "redis:alpine"
    volumes:
      - redis_data:/data
    ports:
      - "6379:6379"
  worker:
    build: .
    command: celery worker --app rootapp --loglevel info --logfile celery-worker.log
    volumes:
      - .:/code
    depends_on:
      - redis
  schedule:
    build: .
    command: celery beat --app rootapp --loglevel info --logfile celery-beat.log
    volumes:
      - .:/code
    depends_on:
      - redis
  web:
    build: .
    command: bash -c "python manage.py migrate --noinput && python manage.py runserver 0.0.0.0:8000"
    volumes:
      - .:/code
    ports:
      - "8000:8000"
    depends_on:
      - db
      - redis
  document:
    image: swaggerapi/swagger-ui
    volumes:
      - .:/app
    ports:
      - "1234:8080"
    environment:
      SWAGGER_JSON: /app/docs/openapi.json
volumes:
  postgres_data:
  redis_data:


```
