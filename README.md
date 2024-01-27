# Репозиторий для выполнения домашних заданий курса "Инфраструктурная платформа на основе Kubernetes-2023-12" 

# Выполнено ДЗ №1

 - [+] Основное ДЗ
 - [+] Задание со *

## В процессе сделано:
 - Установлено и настроено - minikube, kubectl
 - Dockerfile для  Nginx
 - Из Dockerfile собран образ
 - Готовый образ загружен в локальное хранилище minikube
 - Подготовлен манифест namespace.yaml для namespace с именем homework
 - Создан манифест pod.yaml
## Как запустить проект:
 - Перейти в директорию Redrrah_repo/kubernetes-intro/nginx
 - Собрать образ командой  docker build -t redrrah/nginx:v3 .
 - Загрузить образ в minikube minikube image load redrrah/nginx:v3
 - Сменить директорию на Redrrah_repo/
 - Создать namespace с именем homework командой kubectl apply -f kubernetes-intro/namespace.yaml
 - Создать под командой kubectl apply -f kubernetes-intro/pod.yaml
 - Прокинуть порт командой kubectl -n homework port-forward pod/web 8000:8000

## Как проверить работоспособность:
 - Например, перейти по ссылке http://localhost:8000
 - Вариант для терминала curl http://localhost:8000
 Результат вывод - homework #1

## PR checklist:
 - [+] Выставлен label с темой домашнего задания