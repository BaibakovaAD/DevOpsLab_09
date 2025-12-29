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
<img width="881" height="361" alt="image" src="https://github.com/user-attachments/assets/9d00702a-7dbf-43fc-8313-d06abb2af759" />

Загружаем готовый образ redis внутрь кластера и просматриваем доступность образов.
<img width="816" height="298" alt="image" src="https://github.com/user-attachments/assets/c7c2dbbb-9d3d-4a4d-b2dd-faa10914e8f2" />

Подготавливаем манифесты:
/flask_redis_k8s/flask.yml
<img width="684" height="697" alt="image" src="https://github.com/user-attachments/assets/93a16941-cd83-4d6c-a14b-8f5237d1168f" />

/flask_redis_k8s/flask-service.yml
<img width="665" height="541" alt="image" src="https://github.com/user-attachments/assets/4f1d3c1f-d6ea-444c-8fe6-550c714ca3f9" />

/flask_redis_k8s/redis.yml
<img width="736" height="647" alt="image" src="https://github.com/user-attachments/assets/4a13183d-d297-47fa-a33e-67e9bd16a692" />

/flask_redis_k8s/redis-service.yml
<img width="728" height="443" alt="image" src="https://github.com/user-attachments/assets/74e33030-acfa-4a6d-81ed-4be6ea17566c" />

Применяем манифесты k8s, проверяем статус реплик и сервисы.
<img width="921" height="464" alt="image" src="https://github.com/user-attachments/assets/a9205896-d6bd-41ef-85af-6eee1ddc32c8" />

Проверяем доступность вебсайта, предварительно запустив в отдельном окне терминала проброс трафика ВМ внутрь minikube.
<img width="1280" height="366" alt="image" src="https://github.com/user-attachments/assets/f3b6fc2b-1eba-4d54-a954-7651a0a58661" />

Обновлем приложение до новой версии.
<img width="857" height="522" alt="image" src="https://github.com/user-attachments/assets/4f1d5c29-52c7-4675-8549-8638eb6f7366" />

Обновляем файл манифеста и применяем его заново.
<img width="865" height="193" alt="image" src="https://github.com/user-attachments/assets/b723b3de-0dfd-4e2f-ad4e-eb5d39dfb62b" />

Далее патчим описание, а также видим как пересоздаются реплики подов.
<img width="871" height="88" alt="image" src="https://github.com/user-attachments/assets/a981e6b4-1b7b-4e21-8f15-8b6459b80714" />
<img width="871" height="490" alt="image" src="https://github.com/user-attachments/assets/b553f10c-2fe8-485c-9267-0ae3948070d4" />
<img width="887" height="88" alt="image" src="https://github.com/user-attachments/assets/c288f7a4-3f7a-422d-990d-5f90b77a0abc" />

Проверяем обновленную версию нашего веб-сервиса.
<img width="1280" height="451" alt="image" src="https://github.com/user-attachments/assets/569b2f06-2b60-400f-9085-7b129da9222d" />

Видим как происходит заменя старых версий подов на новые.
<img width="965" height="705" alt="image" src="https://github.com/user-attachments/assets/08cc13a5-72ef-4dee-990a-f8ced5e74e29" />
<img width="1106" height="649" alt="image" src="https://github.com/user-attachments/assets/978be7c0-60d2-42e9-8160-a49353778f84" />
