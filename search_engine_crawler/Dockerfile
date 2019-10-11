FROM python:3.7.4-alpine

WORKDIR /app
COPY . /app

RUN pip install -r requirements.txt

ENV EXCLUDE_URLS '.*github.com'

ENTRYPOINT ["python", "-u", "crawler/crawler.py"]
CMD ["https://vitkhab.github.io/search_engine_test_site/"]
