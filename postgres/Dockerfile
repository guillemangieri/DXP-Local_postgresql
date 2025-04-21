FROM postgres:13

# Copia o arquivo de configuração de autenticação
COPY pg_hba.conf /etc/postgresql/pg_hba.conf

# Script de inicialização (opcional)
COPY init.sql /docker-entrypoint-initdb.d/

# Garante permissões
RUN chmod 600 /etc/postgresql/pg_hba.conf && \
    chmod 644 /docker-entrypoint-initdb.d/init.sql

EXPOSE 5432