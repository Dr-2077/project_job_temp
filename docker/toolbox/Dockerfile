FROM alpine
RUN apk update && apk add --no-cache curl wget busybox-extras netcat-openbsd python3 py3-pip && \
    python3 -m venv /env
RUN /env/bin/pip install awscli
RUN apk --purge -v del py3-pip
CMD tail -f /dev/null
