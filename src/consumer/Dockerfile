FROM python:3.10-alpine
RUN /usr/local/bin/python -m pip install --upgrade pip
RUN pip freeze > requirements.txt
RUN pip install -r requirements.txt
WORKDIR /src
RUN pip install requests
COPY consumer.py .
ENTRYPOINT ["python"]
CMD ["consumer.py"]


