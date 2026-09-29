# docker-flask-app

App Flask mínimo com Dockerfile para publicação no Docker Hub.

## Rodar localmente (sem Docker)
```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python app.py
```
Acesse http://localhost:8000


## Build e push (Docker Hub)
Substitua `SEU_USUARIO` pelo seu login no Docker Hub:
```bash
docker build -t SEU_USUARIO/docker-flask-app:latest .
docker build -t ellenyass/docker-flask-app:latest .
docker login
docker push SEU_USUARIO/docker-flask-app:latest
docker push ellenyass/docker-flask-app:latest
```
## Rodar a imagem
```bash
docker run --rm -p 8000:8000 SEU_USUARIO/docker-flask-app:latest
docker run --rm -p 8000:8000 ellenyass/docker-flask-app:latest
```