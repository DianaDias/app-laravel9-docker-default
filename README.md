
### Passo a passo
Clone Repositório
```sh
git clone https://github.com/DianaDias/app-laravel9-docker-default.git nome-projeto-novo
```

```sh
cd nome-projeto-novo/
```

Remova o versionamento
```sh
rm -rf .git/
```

Crie o Arquivo .env
```sh
cd example-project/
cp .env.example .env
```

Altere o arquivo docker-compose.yml na linha 6 para o nome do seu projeto atual
Exemplo:
    container_name: app-novo-laravel

Altere o ARG user= para o seu nome
Exemplo: 
    ARG user=diana    


Inicie o repositorio que irá trabalhar
```sh
git init
```

Adicione o repositorio novo que irá trabalhar
```sh
git remote add origin https://github.com/DianaDias/nome-do-repositorio-novo.git
```

Atualize as variáveis de ambiente do arquivo .env do banco
```dosini

DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=nome_que_desejar_db
DB_USERNAME=root
DB_PASSWORD=root

```


Suba os containers do projeto
```sh
docker-compose up -d
```

Acesse o projeto
[http://localhost:8180](http://localhost:8180)
