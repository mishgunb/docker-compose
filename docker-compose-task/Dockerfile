# Базовый образ — официальный nginx (берем Alpine)
FROM nginx:1.25-alpine

# Метаданные образа
LABEL maintainer="Mikhail"
LABEL description="Web server image (nginx) for Docker Compose assignment"

# Копируем каталог с файлами настроек nginx внутрь контейнера, 
# заменяя дефолтный конфиг сервера
COPY ./nginx-config/ /etc/nginx/conf.d/

# Копируем index.html в каталог, который nginx отдаёт по умолчанию
COPY ./html/ /usr/share/nginx/html/

# Документируем порт, на котором слушает сервер внутри контейнера
EXPOSE 80

