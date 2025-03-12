FROM node:20-alpine
WORKDIR /web
COPY . /web

RUN addgroup -S mercari && adduser -S trainee -G mercari
USER trainee


CMD ["uvicorn", "main:web", "--host", "0.0.0.0", "--port", "3000"]
