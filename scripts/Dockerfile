FROM apache/airflow:2.10.0

USER root

# Instalar dependências do sistema
RUN apt-get update && apt-get install -y \
    libpq-dev \
    gcc \
    gosu \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

USER airflow

# Atualizar psycopg2 para suportar SCRAM
RUN pip install --no-cache-dir --upgrade \
    psycopg2-binary>=2.9.0