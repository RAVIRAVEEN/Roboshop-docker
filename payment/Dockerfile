FROM python:3.9.19-alpine3.20

EXPOSE 8080
USER root
ENV AMQP_USER=roboshop \
    AMQP_PASS=roboshop123 
WORKDIR /app
COPY requirements.txt /app/
RUN pip install -r requirements.txt
COPY *.py /app/
COPY payment.ini /app/
#CMD ["python", "payment.py"]
CMD ["uwsgi", "--ini", "payment.ini"]