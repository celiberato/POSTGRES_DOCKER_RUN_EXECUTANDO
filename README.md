# POSTGRES_DOCKER_RUN_EXECUTANDO

# Atualiar os pacotes do linux
sudo apt update

# Baixar iagem do postgres
docker pull postgres

# Executar o container
docker run --name postgres_container -e POSTGRES_PASSWORD=mysecretpassword -d postgres

# reinicar o serviço
sudo systemctl start postgresql
sudo systemctl enable postgresql

# Excutar scripts no 
CREATE DATABASE meu_banco;
## Criar usuário
CREATE USER meu_usuario WITH ENCRYPTED PASSWORD 'minha_senha';  

## Privilégios
GRANT ALL PRIVILEGES ON DATABASE meu_banco TO meu_usuario;  

## Crir banco de dados
CREATE DATABASE meu_banco;

## Executar o postgres
sudo -i -u postgres
psql

## Executar pgadmin4 
docker run -d \
  -p 8080:80 \
  -e PGADMIN_DEFAULT_EMAIL="admin@example.com" \
  -e PGADMIN_DEFAULT_PASSWORD="minha_senha_segura" \
  --name pgadmin_container \
  dpage/pgadmin4
