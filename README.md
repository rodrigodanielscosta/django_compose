# django_compose
Containers python3 e nginx para projetos Django simples.

# Para rodar o projeto

Crie um arquivo .env minimamente com:
SECRET_KEY='sua_secret_key'
DEBUG=1

docker-compose up --build -d

Ao incluir suas apps Django lembre-se de realizar os comandos :

django-compose exec web python manage.py makemigrations

django-compose exec web python manage.py migrate

E outros comandos django que desejar.
