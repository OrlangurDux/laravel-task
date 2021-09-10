## Задача

Делаем форк проекта в свой закрытый репозиторий после выполнения задачи шарим форк на пользователя OrlangurDux для проверки. Необходимо реализовать "абстрактный" драйвер (как вариант отправка email или любой другой метод) и демонстрационную обвязку по работе с ним для Laravel.  

## Использование

Устанавливаем Docker [Docker installed](https://docs.docker.com/docker-for-mac/install/) на вашу систему и клонируем репозиторий.

Создаем папки **src** и **mysql**

Собираем и запускаем контейнеры `docker-compose up -d --build site`.

Запускаем `docker-compose run --rm composer create-project laravel/laravel .`

В дальнейшем запускаем контейнер через `up` пересобираем через `--build site` только в случае изменений. Используемые внешние порты:

- **nginx** - `:8070`
- **mysql** - `:3309`
- **php** - `:9000`
- **redis** - `:6381`
- **mailhog** - `:8025` 

Дополнительные контейнеры для работы с Laravel

- `docker-compose run --rm composer update`
- `docker-compose run --rm npm run dev`
- `docker-compose run --rm artisan migrate` 
