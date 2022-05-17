
# Projeto sistema administrativo da plataforma E-Diaristas

### Passo a passo
#### Crie o Arquivo .env
```sh
cd example-project/
cp .env.example .env
```


#### Atualize as variáveis de ambiente do arquivo .env
```dosini
APP_NAME=Laravel
APP_URL=http://localhost:8180

DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=nome_que_desejar_db
DB_USERNAME=root
DB_PASSWORD=root

CACHE_DRIVER=redis
QUEUE_CONNECTION=redis
SESSION_DRIVER=redis

REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379
```


#### Suba os containers do projeto
```sh
docker-compose up -d
```


#### Acessar o container
```sh
docker-compose exec app bash
```


#### Instalar as dependências do projeto
```sh
composer install
```


#### Gerar a key do projeto Laravel
```sh
php artisan key:generate
```

#### Criar a estrutura no banco de dados

```
php artisan migrate
```

#### Criar o usuário admin

```
php artisan db:seed
```

Usuário criado admin@admin.com  
Senha: 123123123



Acesse o projeto
[http://localhost:8180](http://localhost:8180)
