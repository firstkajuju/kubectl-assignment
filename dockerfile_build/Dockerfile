FROM ubuntu:20.04

# Update package lists and install system-level dependencies
RUN apt-get update -y \
    && apt-get install -y python3-pip \
    && apt-get install -y mysql-client \
    && apt-get install -y wget \
    && apt-get install -y python3 \
    && apt-get install -y python3-dev \
    && apt-get install -y libmysqlclient-dev
COPY . /app
RUN pip install --upgrade pip \
    && pip3 install flask
    
RUN pip install -r requirements.txt


EXPOSE 8080


ENTRYPOINT ["python3"]
CMD ["app.py"]

