# POSTGRES_DOCKER_RUN_EXECUTANDO

# Atualiar os pacotes do linux
sudo apt update

# Instalar o pgadmin4
sudo apt install pgadmin4

# Baixar iagem do postgres
docker pull postgres

# Executar o container
docker run --name postgres_container -e POSTGRES_PASSWORD=mysecretpassword -d postgres

# reinicar o serviço
sudo systemctl start postgresql
sudo systemctl enable postgresql

# Excutar scripts no 
CREATE DATABASE meu_banco;
## CREATE USER meu_usuario WITH ENCRYPTED PASSWORD 'minha_senha';  

## GRANT ALL PRIVILEGES ON DATABASE meu_banco TO meu_usuario;  

## CREATE DATABASE meu_banco;

## sudo -i -u postgres
## psql
## docker run -d \
  -p 8080:80 \
  -e PGADMIN_DEFAULT_EMAIL="admin@example.com" \
  -e PGADMIN_DEFAULT_PASSWORD="minha_senha_segura" \
  --name pgadmin_container \
  dpage/pgadmin4
