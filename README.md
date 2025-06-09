# POSTGRES_DOCKER_RUN_EXECUTANDO


sudo apt update
sudo apt install pgadmin4

docker pull postgres
docker run --name postgres_container -e POSTGRES_PASSWORD=mysecretpassword -d postgres

sudo systemctl start postgresql
sudo systemctl enable postgresql

CREATE DATABASE meu_banco;

CREATE USER meu_usuario WITH ENCRYPTED PASSWORD 'minha_senha';  

GRANT ALL PRIVILEGES ON DATABASE meu_banco TO meu_usuario;  

CREATE DATABASE meu_banco;

sudo -i -u postgres
psql
docker run -d \
  -p 8080:80 \
  -e PGADMIN_DEFAULT_EMAIL="admin@example.com" \
  -e PGADMIN_DEFAULT_PASSWORD="minha_senha_segura" \
  --name pgadmin_container \
  dpage/pgadmin4
