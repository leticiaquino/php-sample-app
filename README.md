NAC RM76577 - Sistemas para Internet | DevOps
=================================================


INSTRUÇÕES DE EXECUÇÃO DA APLICAÇÃO:
------------------------------------

Para a execução da aplicação, primeiramente instale o Docker Toolbox em seu computador.

Link para instalação: [Docker Toolbox](https://docs.docker.com/toolbox/overview/)

Feito isso, o próximo passo é utilizar o terminal *Docker Quickstart* e acessar o diretório onde foi feito o download do seu repositório
```bash
$ cd C:/Docker/php-sample-app-master
```
Ou acesse diretamente pelo Github
```bash
$ git clone https://github.com/leticiaquino/php-sample-app.git
```

Para listar o conteúdo dentro do diretório, use o comando 'ls':
```bash
$ls
```

Faça o *pull* da imagem do PHP e MYSQL do repositório do Docker

* Foi utilizado a [versão 7.2 do PHP com APACHE](https://hub.docker.com/_/php/)

* E a [versão 5.7 do MYSQL](https://hub.docker.com/_/mysql/)

* [Para encontrar essa versão e outras clique aqui.](https://hub.docker.com/)

Agora faça o *pull* da imagem do PHP com Apache:
```bash
$ docker pull php:7.2-apache
```
E faça o *pull* da imagem do MYSQL:
```bash
$ docker pull mysql:5.7
```
O comando *docker images* é utilizado para verificar se as imagens estão no repositório após ter feito o *pull* anteriormente.

```bash
$ docker images
```
Digite o comando abaixo para *buildar* a imagem no backend e insira a versao (Ex: 0.1)
```bash
docker build ./backend -t backend-mysqli:0.1
```

Digite o comando abaixo para *buildar* a imagem do frontend e insira a versao (Ex: 0.1)
```bash
docker build ./frontend -t php:7.2-apache:0.1
```

Rodando o container do backend:
```bash
docker run -d --rm --name backend -e MYSQL_DATABASE=demo -e MYSQL_ALLOW_EMPTY_PASSWORD=yes backend-mysql:0.1
```
Rodando o container do frontend:
```bash
docker run -d --rm --name frontend -p 80:80 --link backend frontend-php:0.1
```

Acessando a aplicação:
```bash
http://localhost
```
ou
```bash
http://192.168.99.100
```

```
