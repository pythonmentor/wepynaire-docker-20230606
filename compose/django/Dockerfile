FROM python:3.11.3-bullseye

# Définir votre répertoire de travail
WORKDIR /app


# Installer les dépendances et mettre à jour les paquets de l'image
RUN apt-get update && apt-get install -y --no-install-recommends \
    # dépendances à installer selon la doc de psycopg2: https://www.psycopg.org/docs/install.html#build-prerequisites
    build-essential \
    libpq-dev

# Copier notre requirements.txt ou Pipfile*
COPY ./Pipfile ./Pipfile.lock .
# ou COPY ./requirements.txt .

# Installer les dépendances python
RUN pip install pipenv && pipenv sync --system --dev 
# ou RUN pip install -r requirements

# Copier nos fichier de projets
COPY . .

# Eliminer les caractères indésirables générés sous windows pourt les scripts bash
RUN sed -i 's/\r//g' /app/compose/django/entrypoint 
# Rendre le script exécutable
RUN chmod +x /app/compose/django/entrypoint

RUN sed -i 's/\r//g' /app/compose/django/start 
RUN chmod +x /app/compose/django/start

ENTRYPOINT ["/app/compose/django/entrypoint"]