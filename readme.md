Projeto utilizando Celery com RabbitMQ e Flower para visualização

Instalar dependências do projeto:
pip install -r requirements.txt

Iniciar RabbitMQ:
docker-compose up

Rodar Celery:
celery -A task worker -l info --pool=solo

Rodar Celery usando Flower:
celery -A task flower --address=127.0.0.6 --port=5566
