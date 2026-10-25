# Flask API with Docker and CI



![Flask API CI](https://github.com/ahmadbilal99p/flask-api/actions/workflows/ci.yml/badge.svg)



A small Flask API packaged with Docker and tested automatically with GitHub Actions on every push.

## Endpoints
- `/` returns a hello message
- `/health` returns the health status

## Run it yourself
```bash
docker build -t flask-api .
docker run -d -p 5000:5000 flask-api
curl http://localhost:5000/health
```

## CI pipeline
On every push, GitHub Actions builds the Docker image, starts the container and checks that `/health` responds with "healthy".
