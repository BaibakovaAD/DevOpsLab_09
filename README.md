# DevOpsLab_09 Kuber basics

Устанавливаем minikube на виртуальную машину. Для этого скачиваем и инсталлируем minikube, добавляем себе права и отключаем своп.
<img width="856" height="482" alt="image" src="https://github.com/user-attachments/assets/0812c306-896d-4828-bee9-c02549c8136c" />

Запускаем minikube в режим однонодового кластера k8s.
<img width="803" height="197" alt="image" src="https://github.com/user-attachments/assets/4d58bc88-ddef-4208-b652-c0452b44d587" />
<img width="850" height="259" alt="image" src="https://github.com/user-attachments/assets/c65ac5ff-82df-4c5a-b016-e953f4ceac27" />

Проверяем minikube и k8s кластера на виртуальной машине.
<img width="614" height="295" alt="image" src="https://github.com/user-attachments/assets/104cb23f-38cf-46a9-abd2-ab9ea126cf07" />

Организуем древовидную файловую структуру.
<img width="632" height="340" alt="image" src="https://github.com/user-attachments/assets/ed2d2bbc-75e4-429f-8510-35d080fc1844" />

Добавляем вывод имени реплики приложения на веб-страницу в приложении flask.
<img width="1163" height="479" alt="image" src="https://github.com/user-attachments/assets/f8e0d722-6e0e-4b04-9703-0d59f4d758de" />

Подготавливаем образы контейнеров и делаем их доступными в кластере k8s.
Производим сборку образа из исходников прямо внутри minikube.
<img width="961" height="422" alt="image" src="https://github.com/user-attachments/assets/622a0576-5e68-495f-9a12-26e43f886d72" />

Загружаем готовый образ redis внутрь кластера и просматриваем доступность образов.
<img width="796" height="303" alt="image" src="https://github.com/user-attachments/assets/431ff960-f5a0-4ff0-a330-6c2ff1e99af5" />

Подготавливаем манифесты:
/flask_redis_k8s/flask.yml
<img width="850" height="691" alt="image" src="https://github.com/user-attachments/assets/e02b4763-9313-448e-9db4-b42e63506f7c" />

/flask_redis_k8s/flask-service.yml
<img width="818" height="460" alt="image" src="https://github.com/user-attachments/assets/db0c11e4-52ec-47f9-bf3f-74a029a70edc" />

/flask_redis_k8s/redis.yml
<img width="886" height="629" alt="image" src="https://github.com/user-attachments/assets/1db46b7a-2ffd-4974-9d7a-6ddc4376263d" />

/flask_redis_k8s/redis-service.yml
<img width="800" height="489" alt="image" src="https://github.com/user-attachments/assets/1885996d-32e0-432e-9df6-8e46d80fd073" />

Применяем манифесты k8s, проверяем статус реплик и сервисы.
<img width="855" height="143" alt="image" src="https://github.com/user-attachments/assets/719c8297-c47d-4837-b670-dffb2331dcd6" />
<img width="676" height="214" alt="image" src="https://github.com/user-attachments/assets/567e4bcd-9cd1-4f2e-8a0d-7715fc40772d" />
<img width="895" height="153" alt="image" src="https://github.com/user-attachments/assets/0647d094-6a8f-499b-b404-2233e76fdf70" />

Проверяем доступность вебсайта, предварительно запустив в отдельном окне терминала проброс трафика ВМ внутрь minikube
