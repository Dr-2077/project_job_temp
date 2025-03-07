FROM alpine

# Обновление индекса репозиториев и установка необходимых пакетов
RUN apk update && apk add --no-cache curl wget busybox-extras netcat-openbsd python3 py3-pip

# Создание виртуальной среды и установка awscli
RUN python3 -m venv /env
RUN /env/bin/pip install awscli

# Очистка пакета pip после установки
RUN apk --purge -v del py3-pip

# Установка команды по умолчанию
CMD tail -f /dev/null
