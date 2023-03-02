FROM python:3.11.0

RUN python -m pip install paho.mqtt

COPY publisher.py .

ENTRYPOINT ["python", "publisher.py"]