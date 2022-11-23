## В сборке
- PHP 7.3 (opcache, xdebug)
- nginx 1.14
- mysql 5.7
- elasticsearch 7.9.1
- smtp (иммитация, перехват писем небольшим скриптом на go)
- mailhog для просмотра писем

Соответствует всем тестам на БУС

## Установка зависимостей
- Git
```
sudo apt-get install -y git
```
- Docker
```
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
sudo groupadd docker
sudo usermod -aG docker $USER
```

- Docker compose
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.24.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

## Начало работы
- Склонируйте репозиторий bitrix-docker
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

Bitrix проект нужно расположить в папке `www`

### Установка через `bitrixsetup.php`
- Скачайте `bitrixsetup.php` (файл будет скачан с официального сайта автоматически)

В nginx сейчас заданы настройки для http://rosa.local

### Востановление через `restore.php`
- Скачайте `restore.php` (файл будет скачан с официального сайта автоматически)
```

- Востановление будет доступна по адресу `http://rosa.local/restore.php`

## Использование

### Mailhog 
Mailhog (почтовый клиент) все письма из системы будут отображены в почтовом клиенте. Доступен по адресу http://rosa.local:8025/
