## В сборке
- PHP 8.1 (opcache, xdebug)
- nginx 1.14
- mysql 5.7
- elasticsearch 7.9.1
- smtp (иммитация, перехват писем небольшим скриптом на go)
- mailhog для просмотра писем
- redis

## Начало работы
```

- Выполните настройку окружения

Скопируйте файл `.env.example` в `.env`

```
cp .env.example .env
```

- Запустите bitrix-docker

```
docker-compose up --build -d
```

## Установка bitrix

Bitrix проект нужно расположить в папке `www/site`

### Установка через `bitrixsetup.php`
- Скачайте `bitrixsetup.php` (файл будет скачан с официального сайта автоматически)

В nginx сейчас заданы настройки для http://your_site.local

### Востановление через `restore.php`
- Скачайте `restore.php` (файл будет скачан с официального сайта автоматически)
```

- Востановление будет доступна по адресу `http://your_site.local/restore.php`

## Использование

### Mailhog 
Mailhog (почтовый клиент) все письма из системы будут отображены в почтовом клиенте. Доступен по адресу http://your_site.local:8025/
