## Deploying a model as a web-service

* Creating a virtuaç environment with Pipenv
* Creating a script for predictions
* Putting the script into a Flask app
* Packaging the app to Docker

```
bash
docker build -t ride-duration-prediction-service:v1 .
```

```
bash
docker run -it --rm -p 9696:9696 ride-duration-prediction-service:v1
```



'''
pipenv install gunicorn

O Gunicorn (Green Unicorn) é um servidor WSGI (Web Server Gateway Interface) amplamente utilizado para aplicações web Python. Ele é projetado para ser leve, simples e altamente eficiente, permitindo que aplicações web em frameworks como Flask, Django ou qualquer aplicação Python compatível com WSGI sejam servidas com desempenho elevado em produção.


gunicorn --bind=0.0.0.0:9696 predict:app
'''