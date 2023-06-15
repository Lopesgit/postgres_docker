# postgres_docker

Criar arquivo ***.env*** com as seguintes variáveis:
```
POSTGRES_USER=
POSTGRES_PASSWORD=
POSTGRES_DB=
```
Desta forma serão definidos o usuário padrão (POSTGRES_USER) e sua respectiva senha (POSTGRES_PASSWORD), assim como será definido o banco de dados inicial (POSTGRES_DB).

## pgadmin4
Caso queira usar o pgadmin4 basta descomentar os trechos de código no arquivo ***docker-compose.yml*** indicados abaixo:
```
  # pgadmin:
  #   image: dpage/pgadmin4
  #   restart: always
  #   env_file:
  #     - .env
  #   ports:
  #     - 15432:80
  #   volumes:
  #     - ./pgadmin_storage:/var/lib/pgadmin/storage
  #   networks:
  #     - postgres-network
```
E também adicionar no arquivo ***.env*** as seguintes variáveis:
```
PGADMIN_DEFAULT_EMAIL=
PGADMIN_DEFAULT_PASSWORD=
```

**Obs.:** o arquivo ***.env.example*** contém as *keys* das variávies utilizadas para este projeto.