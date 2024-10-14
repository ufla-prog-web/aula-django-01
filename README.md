# Aula Django 01 - Visão Geral do Django

<p align="center">
  <a href="#">
    <img src="https://img.shields.io/badge/Aula-Python-brightgreen.svg" alt="Aula Python">
  </a>
  <a href="#">
    <img src="https://img.shields.io/badge/Aula-Django-blue.svg" alt="Aula Django">
  </a>
  <a href="#">
    <img src="https://img.shields.io/badge/Aula-Backend-orange.svg" alt="Aula Backend">
  </a>
</p>

## Índice

* [Introdução](#introdução)
* [Recursos Utilizados](#recursos-utilizados)
* [Fundamentos Teóricos](#fundamentos-teóricos)
* [Objetivo da Aula](#objetivo-da-aula)
* [Desenvolvimento do Projeto](#desenvolvimento-do-projeto)
* [Créditos e Referências](#créditos-e-referências)

## Introdução

Aula Django 01. Projeto utilizando o Django para ser desenvolvido na Aula de GAC116 - Programação Web.

O objetivo desse projeto é mostrar uma visão geral do framework Python Django em que as principais funcionalidades do Django são apresentadas.

Este tutorial foi elaborado baseado no tutorial disponível no [curso de django da w3schools](https://www.w3schools.com/django/index.php) e também baseado na [documentação oficial do django](https://docs.djangoproject.com/pt-br/5.0/).

A aula está estruturada em forma de tutorial, de forma que cada estudante vá replicando em seu computador os conceitos e recursos aqui mostrados. A aula mostra a evolução do código/solução para que os estudantes possa compreender como as diferentes tecnologias se conectam.

## Recursos Utilizados

A seguir estão listados os principais recursos utilizados no desenvolvimento desta aula.

### Linguagens

* Python - Linguagem de Programação Principal
  * [link do site python](https://www.python.org/)
  * [link do curso da w3schools](https://www.w3schools.com/python/default.asp)
* HTML - Estrutura da Página Web
  * [link do curso da w3schools](https://www.w3schools.com/html/default.asp)
* SQL - Linguagem para Consultas no Banco de Dados
  * [link do curso da w3schools](https://www.w3schools.com/sql/default.asp)

### Frameworks

* Django - Framework Web
  * [link do site do django](https://www.djangoproject.com/)
  * [link do curso da w3schools](https://www.w3schools.com/django/index.php)

### Bibliotecas

* Jinja - Biblioteca Python para Templates
    * [link do site do jinja](https://jinja.palletsprojects.com/en/3.1.x/)

### Ferramentas

* Git - Sistema de Controle de Versão - [link](https://git-scm.com/)
* Github - Plataforma de Hospedagem de Códigos - [link](https://github.com/)
* Visual Studio Code - IDE - [link](https://code.visualstudio.com/)
* Pip - Gerenciador de Pacotes do Python - [link](https://pypi.org/project/pip/)
* Venv - Ambiente Virtual do Python - [link](https://docs.python.org/pt-br/3/library/venv.html)
* SQLite Online - SGBD - [link](https://sqliteonline.com/)
* DB Browser for SQLite - SGBD - [link](https://sqlitebrowser.org/)

## Fundamentos Teóricos

A seguir estão destacados alguns dos principais fundamentos teóricos para entendimento desse tutorial.

### Características do Django

**1. Framework completo:** Django oferece tudo o que é necessário para o desenvolvimento de uma aplicação web, incluindo roteamento de URLs, mapeamento objeto-relacional (ORM), sistema de templates, autenticação, etc.

**2. Administração automática:** Com base nos modelos definidos, Django gera automaticamente uma interface administrativa poderosa e personalizável, economizando tempo no desenvolvimento de funcionalidades administrativas.

**3. ORM (Object-Relational Mapping):** O Django possui um ORM que facilita a interação com bancos de dados relacionais, permitindo que os desenvolvedores escrevam consultas em Python ao invés de SQL.

**4. Sistema de templates:** Django possui um sistema de templates eficiente que permite criar HTML dinâmico de forma organizada, utilizando lógica básica como laços e condicionais.

**5. Segurança embutida:** O Django se preocupa com a segurança, oferecendo proteção contra ataques comuns como SQL Injection, Cross-site Scripting (XSS), Cross-site Request Forgery (CSRF), e Clickjacking.

**6. Escalabilidade:** Django é altamente escalável, podendo lidar com grandes volumes de tráfego, como em sites populares que utilizam o framework (por exemplo, Instagram e Pinterest).

**7. Comunidade ativa e documentação:** Django conta com uma ampla comunidade de desenvolvedores e uma documentação completa e detalhada, facilitando a resolução de problemas e o aprendizado.

**8. Reutilização de código:** Django promove a reutilização de componentes por meio de pacotes chamados "apps". Cada app é modular e pode ser usado em diferentes projetos ou em diferentes partes da mesma aplicação.

**9. Suporte a várias bases de dados:** O Django suporta diferentes sistemas de banco de dados, como PostgreSQL, MySQL, SQLite e Oracle, tornando-o flexível para diversos ambientes.

**10. Testes integrados:** O Django tem suporte nativo para testes automatizados, permitindo que desenvolvedores escrevam e executem testes facilmente para garantir a qualidade do código.

### Arquitetura Web de Três Camadas

A arquitetura web de três camadas é um padrão de design de software que organiza uma aplicação em três níveis distintos, cada um com responsabilidades bem definidas. Essas camadas são:

**1. Camada de Apresentação (Frontend)**:

* Também chamada de interface de usuário, essa camada é responsável pela interação com o usuário. Ela inclui tudo o que o usuário vê e utiliza para interagir com o sistema, como páginas web, formulários, botões, e elementos visuais em geral.
* Aqui, são usados tecnologias como HTML, CSS, JavaScript e frameworks frontend (React, Angular, etc.).
* A camada de apresentação envia as entradas dos usuários para a camada de negócios e exibe os resultados de volta para o usuário.

**2. Camada de Negócios (Lógica da Aplicação - Backend)**:

* Nessa camada está a lógica de negócios da aplicação, ou seja, as regras que governam como os dados devem ser processados e as operações que devem ser realizadas. Ela trata os pedidos recebidos da camada de apresentação e executa as operações necessárias.
* Essa camada pode incluir validações, cálculos e chamadas ao banco de dados. Em termos de tecnologia, é geralmente desenvolvida com linguagens de programação como Python, Java, PHP, ou frameworks como Django, Spring Boot, Laravel, etc.

**3. Camada de Dados (Banco de Dados - Backend)**:

* A camada de dados gerencia o armazenamento e recuperação de dados em um banco de dados. Ela é responsável pela persistência dos dados e operações como criar, ler, atualizar e deletar (CRUD).
* Geralmente, são usados sistemas de gerenciamento de banco de dados relacionais (como MySQL, PostgreSQL) ou não relacionais (como MongoDB).
* A camada de negócios interage com essa camada para armazenar e buscar dados conforme necessário.

**Fluxo da Arquitetura de Três Camadas**:

* O usuário interage com a Camada de Apresentação.
* A Camada de Apresentação faz requisições para a Camada de Negócios.
* A Camada de Negócios processa a lógica e, se necessário, interage com a Camada de Dados.
* A Camada de Dados responde com os dados necessários para a Camada de Negócios.
* A Camada de Negócios retorna os resultados processados para a Camada de Apresentação.
* A Camada de Apresentação exibe os resultados para o usuário.

Essa separação facilita a manutenção e escalabilidade da aplicação, permitindo que cada camada possa ser modificada ou melhorada de forma independente.

![Arquitetura das Aplicações Web](./docs/arquitetura-web.png)

### Arquitetura MVT do Django

O modelo MVT (Model-View-Template) é uma arquitetura usada no framework Django para desenvolvimento de aplicações web. Ele organiza a aplicação em três componentes principais:

* **Model (Modelo)**: Responsável pela definição da estrutura dos dados e a interação com o banco de dados. Ele define as classes que representam as tabelas e seus relacionamentos, além de métodos para realizar consultas e operações nos dados.

* **View (Visão)**: Contém a lógica da aplicação. A view recebe as requisições dos usuários, processa os dados (geralmente acessando o Model), e retorna uma resposta, como uma página HTML renderizada ou dados em formato JSON.

* **Template (Apresentação)**: É a camada de apresentação, onde o conteúdo dinâmico gerado pela View é inserido em arquivos HTML. Os templates permitem a separação da lógica de negócio da interface de usuário, tornando o código mais organizado.

Diferente do padrão MVC, onde o controller gerencia a lógica de controle, no Django, a função das views cumpre esse papel, enquanto os templates gerenciam a apresentação.

A figura abaixo detalha os componentes descritos acima.

![Arquitetura MVT - Geral](./docs/mvt-1.png)

No modelo MVT do Django, as requisições seguem um fluxo bem definido, onde cada componente (Model, View, Template) desempenha um papel específico no processamento e resposta de uma requisição HTTP. O fluxo funciona da seguinte forma:

* **Recebimento da Requisição (HTTP Request)**: Quando um usuário acessa uma URL no navegador, o Django recebe a requisição HTTP correspondente. Esse processo começa no URL *dispatcher* (mapeador de URLs), que verifica qual view deve ser chamada com base na URL requisitada.

* **View (Visão)**: A View é o ponto de entrada para o processamento da requisição. A função ou classe associada à URL recebida é executada. Ela é responsável por: Receber a requisição do usuário; Executar a lógica necessária, que pode incluir validações, processamento de dados, ou interações com o banco de dados através dos Models; e Retornar uma resposta apropriada.

* **Model (Modelo)**: Se a View precisar acessar ou manipular dados, ela fará isso por meio do Model. O Model contém a lógica de negócios relacionada à persistência de dados, permitindo a View realizar operações como criar, ler, atualizar ou deletar registros no banco de dados.

* **Template (Apresentação)**: Após processar os dados, a View geralmente prepara um contexto (um dicionário de dados) e passa esse contexto para o Template. O Template é um arquivo HTML com marcações especiais do Django que permitem a inserção de dados dinâmicos. O Template renderiza esses dados em uma estrutura HTML, exibindo o conteúdo adequado com base nas informações passadas pela View.

* **Resposta (HTTP Response)**: Depois que o Template é renderizado, a View retorna uma resposta HTTP (normalmente uma página HTML ou dados JSON em APIs) ao navegador ou cliente. Essa resposta contém o conteúdo processado e visualizado pelo usuário.

A figura abaixo detalha o fluxo descrito acima.

![Arquitetura MVT - Requisição](./docs/mvt-2.png)

A figura abaixo detalha ainda mais a arquitetura MVT e as tecnologias envolvidas.

![Arquitetura MVT - Detalhes](./docs/mvt-3.png)

### Modelo ORM

O Django suporta o conceito de Mapeamento Objeto-Relacional (ORM). Através do ORM você define a modelagem de dados através de classes em Python. Com isso é possível gerar suas tabelas no banco de dados e manipulá-las sem necessidade de utilizar SQL (o que também é possível). Os registros de cada tabela são representados como instâncias das classes correspondentes.

## Objetivo da Aula

O objetivo da aula é apresentar uma introdução ao framework python django. O Django é utilizado no desenvolvimento de páginas web do lado do servidor, ou seja, é uma ferramenta backend e funciona segundo a arquitetura MVT.

## Desenvolvimento do Projeto

Os passos a seguir devem ser seguidos para alcançar o objetivo da aula.

### Clonando o Repositório

Inicialmente, clone o repositório da seguinte forma:

```bash
git clone https://github.com/ufla-prog-web/aula-django-01.git
```

### Baixando o Repositório

Caso deseje ao invês de clonar o repositório (método acima), baixe o repositório do [link](https://github.com/ufla-prog-web/aula-django-01) clicando em `Code` e `Download ZIP`.

### Instalando o Python

Se necessário, instale o Python (testado na versão 3.10.12) [link](https://www.python.org/downloads/).

Verifique a versão instalada do Python (para ter certeza que tudo ocorreu bem):

```bash
python3 --version
```

### Instalando o Pip

Se necessário, instale o pip (testado na versão 23.2.1):

```bash
sudo apt install python3-pip
```

Verifique a versão instalada do pip (para ter certeza que tudo ocorreu bem):

```bash
pip3 --version
```

### Abrindo o Visual Studio Code

Abra a IDE Visual Studio Code na pasta `aula-django-01`.

**Dica:** Abra o arquivo `README.md` e clique em `Open Preview to the Side` para facilitar a construção da aplicação.

**Dica:** Abra um terminal utilizando a IDE clicando em `Terminal` e `New Terminal`.

### Navegando até a Pasta do Projeto

Inicialmente, navegue no terminal do Visual Studio Code até a pasta `aula-django-01` para realizar as instalações.

```bash
cd aula-django-01
```

### Criando o Ambiente Virtual

Crie o ambiente virtual (venv) para isolar as instalações/dependências do Python:

Unix/macOS

```bash
python3 -m venv venv
```

Windows

```bash
py -m venv venv
```

**OBS:** no comando acima, o segundo nome `venv` é o nome que escolhemos para o nosso ambiente virtual (isso pode ser alterado).

### Ativando o Ambiente Virtual

Ative o ambiente virtual (venv) no seu computador utilizando o comando abaixo:

**Sistema Operacional:** Unix/macOS

```bash
source venv/bin/activate
```

**Sistema Operacional:** Windows

```bash
Set-ExecutionPolicy Unrestricted -Scope Process
.\venv\Scripts\activate.bat
```

Quando desejar sair do ambiente virtual, basta digitar:

```bash
deactivate
```

### Instalando o Django

Instale o django dentro do ambiente virtual criado (testado na versão 5.0.3):

```bash
pip3 install django
```

ou

```bash
python -m pip install Django
```

Verifique a versão instalada do django (para ter certeza que tudo ocorreu bem):

```bash
django-admin --version
```

ou

```bash
python3 -m django --version
```

**OBS:** Caso o terminal não encontre o django-admin, execute o seguinte comando (utilizado geralmente quando não se utiliza o venv no laboratório DCC07):

```bash
export PATH=$PATH:~/.local/bin
```

### Criando o Projeto no Django

Crie um projeto em django utilizando o comando abaixo:

```bash
django-admin startproject mysite .
```

**OBS:** O ponto no comando acima informa ao Django para não criar uma pasta com nome `mysite` dentro de uma pasta `mysite`. Isso evita ter que ficar navegando entre pastas.

### Executando o Projeto

Inicie a execução do projeto django criado utilizando o comando abaixo:

```bash
python3 manage.py runserver
```

**Explicação:** O comando acima é usado no Django para iniciar um servidor de desenvolvimento local. Ele é uma parte fundamental do processo de desenvolvimento web com o Django, pois permite que você execute e teste sua aplicação web em um ambiente de desenvolvimento local antes de implantá-la em um servidor web de produção. Ele inicia um servidor HTTP embutido no Django que pode lidar com solicitações HTTP. Por padrão, o servidor de desenvolvimento escuta na porta 8000, mas você pode especificar uma porta diferente como argumento opcional, por exemplo, `python3 manage.py runserver 8081`.

Acesse através do navegdor web a página [http://127.0.0.1:8000/](http://127.0.0.1:8000/). Uma página padrão do django deve aparecer (semelhante a mostrada abaixo).

![Tela Padrão Django](./docs/tela-django-inicial.png)

### Criando um Aplicativo

Execute o comando abaixo para criar um aplicativo chamado `myapp` dentro do projeto `mysite`:

```bash
django-admin startapp myapp
```

O comando abaixo faz a mesma coisa:

```bash
python3 manage.py startapp myapp
```

**Explicação:** O comando acima é usado para criar uma nova aplicação dentro de um projeto Django. Após executar esse comando, você terá uma nova pasta chamada `myapp` dentro do seu projeto Django, contendo uma estrutura inicial de arquivos Python que você pode começar a editar para construir a lógica da sua aplicação. Uma aplicação (ou app) é um componente reutilizável e modular que realiza uma função específica dentro de um projeto Django. Um projeto Django pode conter várias aplicações, cada uma projetada para lidar com uma parte específica da funcionalidade do site. Cada aplicação é composta por:

* **Models:** Definem a estrutura e o comportamento dos dados. Os modelos são utilizados para interagir com o banco de dados e representar os objetos do mundo real dentro do sistema.

* **Views:** Responsáveis por processar as requisições do usuário e retornar as respostas adequadas. As views são geralmente funções que recebem uma solicitação HTTP e retornam uma resposta HTTP, como uma página da web renderizada ou um objeto JSON.

* **Templates:** Arquivos de templates que definem a aparência das páginas da web. Os templates são usados pelas views para renderizar o conteúdo dinâmico que será enviado ao navegador do usuário.

* **Arquivos Estáticos (opcional):** Como CSS, JavaScript e imagens, que são usados para estilizar e adicionar interatividade às páginas da web.

* **URLs:** Mapeiam as URLs do site para as views correspondentes. Cada aplicação geralmente tem seu próprio arquivo urls.py para definir os padrões de URL específicos dessa aplicação.

### Entendendo a Estrutura de Diretórios do Django

A estrutura de diretórios de um projeto Django é organizada de maneira a separar os diferentes componentes da aplicação, facilitando o desenvolvimento e a manutenção. A seguir, temos a estrutura geral de diretórios de um projeto feito em Django. 

```text
myproject/
│
├── manage.py
├── myproject/
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── app1/
│   ├── migrations/
│   ├── templates/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   └── tests.py
├── app2/
│   ├── migrations/
│   ├── templates/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   └── tests.py
└── static/
```

* **manage.py**: Um script que permite interagir com o projeto Django a partir da linha de comando. Ele é usado para executar comandos como iniciar o servidor, migrar o banco de dados e criar superusuários.
* **myproject/**: Esta pasta contém os arquivos de configuração e o núcleo do projeto Django. Normalmente, o nome da pasta do projeto coincide com o nome do projeto. Aqui estão os arquivos comuns:
  * **__init__.py**: Indica ao Python que essa pasta deve ser tratada como um pacote.
  * **asgi.py**: Ponto de entrada para servidores ASGI (usado para rodar a aplicação em modo assíncrono).
  * **settings.py**: Arquivo de configuração onde você define parâmetros como a conexão com o banco de dados, apps instalados, middleware, etc.
  * **urls.py**: Arquivo que define os mapeamentos de URL do projeto para as views.
  * **wsgi.py**: Ponto de entrada para servidores WSGI (usado para rodar a aplicação em modo síncrono).
* **app/**: O Django incentiva o uso de uma abordagem modular, onde a funcionalidade de uma aplicação é dividida em "apps" individuais. Cada app tem sua própria pasta dentro do projeto e contém a lógica de uma parte específica do sistema.
  * **migrations/**: Contém arquivos de migração que Django usa para gerenciar o banco de dados. Cada migração reflete uma mudança no modelo de dados.
  * **templates/**: Essa pasta contém os arquivos HTML que serão renderizados pelas views. Cada app pode ter sua própria pasta `templates/` ou você pode criar uma pasta `templates/` global na raiz do projeto.
  * **__init__.py**: Marca a pasta como um pacote Python.
  * **admin.py**: Define como os modelos do app serão exibidos na interface administrativa do Django.
  * **apps.py**: Define a configuração do app.
  * **models.py**: Contém a definição dos modelos (classes) que representam as tabelas do banco de dados.
  * **views.py**: Contém as funções ou classes que processam as requisições e retornam as respostas.
  * **urls.py**: Define as rotas específicas para as views deste app.
  * **tests.py**: Contém testes automatizados para a aplicação.
  * **static/**: Essa pasta contém arquivos estáticos, como CSS, JavaScript e imagens. Os arquivos dentro de `static/` são usados para a apresentação visual da aplicação.

### Criando a Primeira View no Django

Primeiramente, edite o arquivo de `views.py` (na pasta `myapp`) e coloque o seguinte conteúdo:

```python
from django.shortcuts import render
from django.http import HttpResponse

def teste(request):
    return HttpResponse("Olá Mundo!")
```

Em seguida, crie um arquivo nomeado `urls.py` na mesma pasta do arquivo `views.py` e digite o código abaixo:

```python
from django.urls import path
from . import views

urlpatterns = [
    path('teste/', views.teste, name='teste'),
]
```

O comando acima, de forma geral, cadastra uma nova rota na sua aplicação. Quando o usuário acessar a rota ou URL [http://127.0.0.1:8000/teste/](http://127.0.0.1:8000/teste/), o método views.teste será chamado.

Existe um arquivo chamado `urls.py` na pasta `mysite`, abra esse arquivo e coloque o seguinte conteúdo nesse arquivo.

```python
from django.contrib import admin
from django.urls import include, path

urlpatterns = [
    path('', include('myapp.urls')),
    path('admin/', admin.site.urls),
]
```

Em seguida, execute o projeto django (veja se está tudo funcionando):

```bash
python3 manage.py runserver
```

Acesse a página [http://127.0.0.1:8000](http://127.0.0.1:8000). Deverá aparecer uma mensagem de erro (*Page not found*) nesta página.

Por fim, acesse a URL: [http://127.0.0.1:8000/teste/](http://127.0.0.1:8000/teste/`) e analise o resultado.

### Atividade 1 - Crie uma Nova View e Nova Rota

Utilizando o exemplo anterior crie uma nova view e uma nova rota para a sua aplicação. Em seguida, faça os testes para verificar se tudo funcionou corretamente.

### Criando o Primeiro Template no Django

Crie uma pasta `templates` dentro da pasta `myapp` e crie um arquivo HTML chamado `paginateste.html`.

Abra o arquivo HTML e insira o seguinte conteúdo:

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Aplicação Django</title>
  </head>
  <body>
    <h1>Olá Mundo!</h1>
    <p>Bem-vindo ao meu primeiro projeto Django!</p>
  </body>
</html>
```

Agora, é necessário modificar a visualização. Abra o arquivo `views.py` e substitua o método de visualização `teste` por este:

```python
from django.http import HttpResponse
from django.template import loader

def teste(request):
    template = loader.get_template('paginateste.html')
    return HttpResponse(template.render())

...

```

Para poder trabalhar com coisas mais complicadas do que "Hello World!", temos que dizer ao Django que um novo aplicativo foi criado. Isso é feito no arquivo `settings.py` da pasta `mysite`. Procure a lista `INSTALLED_APPS[]` e adicione o aplicativo `myapp` que foi criado. Veja o exemplo abaixo:

```python
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'myapp',                      # inclua o app criado aqui
]
```

Em seguida, execute este comando:

```bash
python3 manage.py migrate
```

**OBS:** Este comando aplica as migrações, ou seja, atualiza o esquema do banco de dados de acordo com as mudanças nos modelos.

Em seguida, execute o projeto django (veja se está tudo funcionando):

```bash
python3 manage.py runserver
```

Por fim, acesse a URL [http://127.0.0.1:8000/teste/](http://127.0.0.1:8000/teste/`) e analise o resultado.

### Atividade 2 - Crie uma Nova Página

Utilizando o exemplo anterior crie uma nova página HTML e atualize a view na sua aplicação que você mesmo havia criado na Atividade 1 feita anteriormente. Em seguida, faça os testes para verificar se tudo funcionou corretamente.

### Passando Parâmetros para o Template do Django

Agora, iremos ver como podemos passar alguns parâmetros do Python para o template HTML utilizando tags do Django (através da biblioteca [Jinja](https://jinja.palletsprojects.com/en/3.1.x/)).

Para isso, crie um arquivo HTML com nome `testeparametros.html` na pasta `templates` com o seguinte conteúdo:

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Aplicação Django</title>
  </head>
  <body>
    <h1>Django: Tags de Templates</h1>
    <p>Neste exemplos utilizamos as tags de templates do Django (Jinja)</p>
    <ul>
        <li><b>Nome:</b> {{ nome }} </li>
        <li><b>Idade:</b> {{ idade }} </li>
        <li><b>E-mail:</b> {{ email }} </li>
        <li><b>Telefone:</b> {{ telefone }} </li>
        <li><b>Usuário Ativo:</b> {{ usuarioativo }} </li>
    </ul>
  </body>
</html>
```

Em seguida, edite o arquivo `views.py` na pasta `myapp` e coloque o seguinte conteúdo ao final:

```python
...

def testeparametros(request):
    template = loader.get_template('testeparametros.html')
    context = {
        "nome": "José Silva",
        "idade": 30,
        "email": "jose.silva@email.com",
        "telefone": "3333-1234",
        "usuarioativo": True
    }
    return HttpResponse(template.render(context, request))
```

Em seguida, edite o arquivo nomeado `urls.py` na mesma pasta do arquivo `views.py` e digite o código abaixo:


```python
...

urlpatterns = [
    ...
    path('testeparametros/', views.testeparametros, name='testeparametros') # linha adicionada
]
```

Em seguida, execute o projeto django:

```bash
python3 manage.py runserver
```

Por fim, acesse a URL [http://127.0.0.1:8000/testeparametros/](http://127.0.0.1:8000/testeparametros/`) e analise o resultado.

### Atividade 3 - Passando Novos Parâmetros

Altere o método `testeparametros` no arquivo `views.py` para passar dois novos parâmetros para o tamplate. Dessa maneira, é necessário alterar também o arquivo `testeparametros.html` para receber os dados passados e imprimi-los na tela.

### Criando o Primeiro Modelo no Django

Até esse momento fizemos a nossa aplicação web com interface, com URLs e algum processamento, mas não trabalhamos com Banco de Dados. Os dados estavam inseridos diretamente no código.

Agora, iremos criar o nosso primeiro modelo, um Livro no Banco de Dados SQLite disponível no Django. No Django, os dados são criados em objetos, chamados Modelos, que na verdade são tabelas em um banco de dados.

Primeiramente, iremos criar uma classe chamada `Livro`. Para isso abra o arquivo `models.py` na pasta `myapp` e digite o seguinte conteúdo:

```python
from django.db import models

class Livro(models.Model):
    nome = models.CharField(max_length=255)
    autor = models.CharField(max_length=255)
    ano = models.IntegerField()
```

O código acima irá criar uma Tabela chamada Livro no BD SQLite. Os campos `nome` e `autor` são campos de texto e estão configurados para ter no máximo 255 caracteres. O campo `ano` é um campo numérico inteiro.

**OBS:** Quando criamos o projeto Django, obtivemos um banco de dados SQLite vazio. Ele estava na raiz da pasta `aula-django-01` e possui o nome de arquivo `db.sqlite3`. Por padrão, todos os modelos criados no projeto Django serão criados como tabelas neste banco de dados.

Em seguida, execute o código abaixo para que seja criado a tabela Livro no banco de dados de fato:

```bash
python3 manage.py makemigrations myapp
```

O que resultará nesta saída:

```bash
Migrations for 'myapp':
  myapp/migrations/0001_initial.py
    - Create model Livro
```

O Django cria um arquivo descrevendo as alterações e armazena o arquivo na pasta `/myapp/migrations/` com nome `0001_initial.py`. Abra esse arquivo para analisar o conteúdo. Observe que o Django insere um campo `id` para suas tabelas, que é um número auto incrementado.

A tabela ainda não foi criada, você terá que executar mais um comando, então o Django criará e executará uma instrução SQL, baseada no conteúdo do novo arquivo da pasta `/myapp/migrations/`.

Execute o comando de migração:

```bash
python3 manage.py migrate
```

O que resultará nesta saída:

```bash
Operations to perform:
  Apply all migrations: admin, auth, contenttypes, myapp, sessions
Running migrations:
  Applying myapp.0001_initial... OK
```

### Acessando o Ambiente Administrativo do Django

O Django Admin é uma ferramenta ótima do Django, na verdade é uma interface de usuário CRUD (Criar, Ler, Atualizar, Excluir) para todos os seus modelos!

Para entrar na interface do usuário administrativo, inicie o servidor com este comando:

```bash
python3 manage.py runserver
```

Na janela do navegador, digite na barra de endereço [127.0.0.1:8000/admin/](127.0.0.1:8000/admin/)

A razão pela qual esta URL vai para a página de login do administrador do Django pode ser encontrada no arquivo `urls.py` do seu projeto:

```python
from django.contrib import admin
from django.urls import include, path

urlpatterns = [
    path('', include('myapp.urls')),
    path('admin/', admin.site.urls),
]
```

A lista `urlpatterns[]` recebe solicitações na rota `admin/` e as envia para `admin.site.urls`, que faz parte de um aplicativo integrado que vem com o Django e contém muitas funcionalidades e interfaces de usuário, sendo uma delas a interface de usuário de login.

### Criando um Usuário no Django

Para poder fazer login no ambiente administrativo do Django, precisamos criar um usuário. Isso é feito digitando este comando:

```bash
python3 manage.py createsuperuser
```

O que dará um prompt como esse:

```bash
Username: admin
Email address: 
Password: 
Password (again): 
The password is too similar to the username.
This password is too short. It must contain at least 8 characters.
This password is too common.
Bypass password validation and create user anyway? [y/N]: y
```

**OBS:** Aqui você deve inserir: nome de usuário, endereço de e-mail (você pode simplesmente deixar em branco ou escolher um endereço de e-mail falso) e senha. Em meu caso coloquei usuário `admin` email em branco e senha `admin`. 

Minha senha não atendeu aos critérios, mas este é um ambiente de teste, e opto por criar usuário mesmo assim, digitando `y` gerando assim a saída:

```bash
Superuser created successfully.
```

Agora, reinicie o servidor:

```bash
python3 manage.py runserver
```

Na janela do navegador, digite na barra de endereço [127.0.0.1:8000/admin/](127.0.0.1:8000/admin/)

Preencha o formulário com o nome de usuário e senha corretos (`admin` e `admin`):

Na tela aberta você pode Criar, Ler, Atualizar e Excluir grupos e usuários, mas onde está o modelo de Livro?

O modelo Livro está faltando, como deveria estar. Você tem que informar ao Django quais modelos devem estar visíveis na interface administrativa.

### Incluindo o Modelo Livro na Interface Administrativa

Para incluir o modelo Livro na interface administrativa, temos que dizer ao Django que este modelo deve estar visível na interface administrativa.

Isso é feito em um arquivo chamado `admin.py`, e está localizado na pasta do seu aplicativo, que no nosso caso é a pasta `myapp`.

Abra-o, o mesmo deve estar assim:

```python
from django.contrib import admin

# Register your models here.
```

Insira algumas linhas aqui para tornar o modelo Livro visível na página de administração:

```python
from django.contrib import admin
from .models import Livro

admin.site.register(Livro)
```

Agora, acesse o endereço [127.0.0.1:8000/admin/](127.0.0.1:8000/admin/) e analise o resultado.

### Atividade 4 - Cadastro de Livros

No ambiente administrativo, vá em Livros e clique em Add Livro, em seguida, cadastre três livros quaisquer. Em seguida, faça testes para realizar a exclusão de um livro. Em seguida, faça testes para realizar a atualização de algum dado em algum livro.

### Visualizando o Modelo de Dados

Existem diversas ferramentas que podem ser utilizadas para ver o banco de dados do modelo criado. Uma dessas ferramentas é o [site SQLite Online](https://sqliteonline.com/). Acesse esse site e carregue o banco de dados chamado `db.sqlite3` localizado na raiz do projeto.

Execute o comando abaixo nessa ferramenta para listar os livros que você cadastrou utilizando o ambiente administrativo.

```sql
SELECT * FROM myapp_livro;
```

Uma outra ferramenta que podemos utilizar é o [DB Browser for SQLite](https://sqlitebrowser.org/). Utilize essa ferramenta para abrir o arquivo do BD chamado `db.sqlite3` que está na raiz do projeto e assim ver as modificações no modelo.

### Atividade 5 - Crie um Outro Modelo 

Crie um outro modelo (tabela) em sua aplicação e registre esse modelo. Acesse o ambiente administrativo e realize a inclusão de dados no modelo criado.

## Créditos e Referências

Este tutorial foi inspirado nos seguintes recursos:

* [Documentação oficial do django](https://docs.djangoproject.com/pt-br/5.0/)
* [Curso de Django da w3schools](https://www.w3schools.com/django/index.php)
