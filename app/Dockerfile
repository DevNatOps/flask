FROM python:3.8-slim
RUN /usr/local/bin/python -m pip install --upgrade pip
RUN pip freeze > requirements.txt
RUN pip install -r requirements.txt
WORKDIR /src
RUN pip install Flask
COPY /src .
EXPOSE 8000
ENTRYPOINT ["python"]
CMD ["-u","app.py"]


