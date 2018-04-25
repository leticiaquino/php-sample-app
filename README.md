NAC RM76577 - Sistemas para Internet - SecDevOps
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
**A configuração do [BACKEND](https://github.com/leticiaquino/php-sample-app/tree/master/backend) e do [FRONTEND](https://github.com/leticiaquino/php-sample-app/tree/master/frontend) estão no arquivo README.md de cada pasta.**
