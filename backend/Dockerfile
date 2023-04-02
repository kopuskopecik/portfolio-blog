FROM python:3.7

ENV PYTHONUNBUFFERED 1
ENV PYTHONDONTWRITEBYTECODE 1

RUN mkdir /backend
WORKDIR /backend
COPY . /backend

RUN pip install -r /backend/requirements.txt
# RUN pip install -r /smart_screen/requirements-dev.txt

RUN chmod +x /backend/docker-entrypoint.sh
CMD ["/bin/bash", "/backend/docker-entrypoint.sh"]