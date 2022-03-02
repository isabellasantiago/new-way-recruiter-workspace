# New Way Recruiter Workspace #

Repositório com as configurações para rodar o projeto New Way Recruiter localmente.

A plataforma é composta por:

* API (`submódulo api`)

* Frontend (`submódulo new-way-recruiter-web`)

---

### Clone ###

Os repositórios estão construídos com submódulos do git, portanto para clonar todas as partes do projeto basta rodar:

```
$ git clone --recurse-submodules git@github.com:isabellasantiago/new-way-recruiter-workspace.git
```

Isso irá clonar este repositório e todos seus submódulos.

Após isso, entre em cada submódulo e verifique se todos estão na branch correta (para desenvolvimento, branch `develop`).

Verifique o arquivo `.env` deste repositório, e o de cada submódulo.

O deste repositório, caso não tenha, pode seguir o `example.env` para criar, seguindo as mesmas chaves, só informando os valores corretos.

Caso algum submodulo não tenha o arquivo `.env`, entre nele e procure no seu README sobre o que fazer.

---

### Run ###

Para rodar o projeto localmente, é necessário todos os arquivos `.env` configurados e [Docker](https://docs.docker.com/get-docker/) e [Docker Compose](https://docs.docker.com/compose/install/) devidamente instalados.

Após isso, basta rodar o comando:

```
$ docker-compose up
```

Isso irá subir todos as partes do projeto de uma vez. Caso queira subir somente uma parte separada, basta rodar:
```
// Caso queira subir somente a api por exemplo
$ docker-compose up api
```

Para saber qual o nome dos services que deve ser informado no comando `up`, basta olhar no arquivo `docker-compose.yml` o nome dos services. O nome de cada service neste arquivo é o nome do service que você deve informar no comando `up`.

Para parar os containers, basta rodar

```
$ docker-compose stop
```

Para parar tudo que esta rodando, ou rodar:

```
$ docker-compose stop api
```

Para parar algum service especifico.
