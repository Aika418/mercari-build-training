FROM alpine

RUN apk update && apk add --no-cache python3 python3-pip
RUN pip3 install -r requirements.txt

WORKDIR /app
COPY . /app


RUN addgroup -S mercari && adduser -S trainee -G mercari
RUN chown -R trainee:mercari /path/to/db
USER trainee

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "9000"]
