FROM python:3
ENV PYTHONUNBUFFERED 1
RUN mkdir /code
WORKDIR /code
COPY requirements.txt /code/
RUN pip install -r requirements.txt
COPY ./webplayground /code/
#RUN python manage.py makemigrations
#RUN python manage.py migrate
CMD gunicorn webplayground.wsgi -b 0.0.0.0:8000
