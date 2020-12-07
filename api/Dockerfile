FROM python:3.7-alpine
ENV PYTHONUNBUFFERED 1
WORKDIR "/app"
COPY ./requirements.txt ./
RUN pip install -r requirements.txt
COPY . .

RUN adduser -D user
USER user
CMD [ "python", "manage.py", "runserver", "0.0.0.0:8000" ]