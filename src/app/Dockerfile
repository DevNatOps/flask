FROM python:3.10-alpine
RUN /usr/local/bin/python -m pip install --upgrade pip
RUN pip freeze > requirements.txt
RUN pip install -r requirements.txt
WORKDIR /src
RUN pip install Flask
COPY app.py .
WORKDIR /src/templates
COPY /templates .
WORKDIR /src
ENTRYPOINT ["python"]
CMD ["-u","app.py"]


