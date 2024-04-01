# Aula Django 01 - Visão Geral do Django

<p align="center">
  <a href="#">
    <img src="https://img.shields.io/badge/Aula-Python-brightgreen.svg" alt="Aula Introdução">
  </a>
  <a href="#">
    <img src="https://img.shields.io/badge/Aula-Django-blue.svg" alt="Python">
  </a>
</p>

Este projeto mostra uma visão geral do framework Python Django. E foi baseado no conteúdo ensinado na aula de programação web utilizando como base a [documentação do django](https://docs.djangoproject.com/pt-br/5.0/) e também o [curso de django da w3schools](https://www.w3schools.com/django/index.php).

## Linguagens Utilizadas

* Python
  * [link do site python](https://www.python.org/)
  * [link do curso da w3schools](https://www.w3schools.com/python/default.asp)
* HTML
  * [link do curso da w3schools](https://www.w3schools.com/html/default.asp)

## Frameworks Utilizados

* Django
  * [link do site do django](https://www.djangoproject.com/)
  * [link do curso da w3schools](https://www.w3schools.com/django/index.php)

## Bibliotecas Utilizadas

* Jinja - [link do site do jinja](https://jinja.palletsprojects.com/en/3.1.x/)

## Ferramentas Utilizadas

* Visual Studio Code - [link](https://code.visualstudio.com/)
* SQLite Online - [link](https://sqliteonline.com/)
* Pip - [link](https://pypi.org/project/pip/)
* Venv - [link](https://docs.python.org/pt-br/3/library/venv.html)

## Desenvolvimento do Projeto

Os passos a seguir devem ser seguidos para se ter uma visão geral do framework Django.

### Baixando o Repositório

Inicilamente, baixe o repositório do [link](https://github.com/ufla-prog-web/aula-django-01) clicando em `Code` e `Download ZIP`.

Ou então, clone o repositório através do comando abaixo:

```bash
git clone https://github.com/ufla-prog-web/aula-django-01.git
```

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

### Instalando o Ambiente Virtual

Inicialmente, navegue no terminal até a pasta `aula-django-01` para realizar as instalações.

```bash
cd aula-django-01
```

Instale o ambiente virtual (venv) para isolar as instalações/dependências do Python:

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

Verifique a versão instalada do django (para ter certeza que tudo ocorreu bem):

```bash
django-admin --version
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

Acesse através do navegdor web a página [http://127.0.0.1:8000/](http://127.0.0.1:8000/). Uma página padrão do django deve aparecer.

### Criando um Aplicativo

Execute o comando abaixo para criar um aplicativo chamado `myapp` dentro do projeto `mysite`:

```bash
python3 manage.py startapp myapp
```

O comando abaixo faz a mesma coisa:

```bash
django-admin startapp myapp
```

### Criando a Primeira View no Django

Edite o arquivo de `views.py` (na pasta `myapp`) e coloque o seguinte conteúdo:

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

OBS: deve aparecer uma mensagem de erro (Page not found) na página [http://127.0.0.1:8000](http://127.0.0.1:8000).

OBS: assim, acesse a URL: [http://127.0.0.1:8000/teste/](http://127.0.0.1:8000/teste/`).

### Criando o Primeiro Template no Django

Crie uma pasta `templates` dentro da pasta `myapp` e crie um arquivo HTML chamado `paginateste.html`.

Abra o arquivo HTML e insira o seguinte:

```html
<!DOCTYPE html>
<html>
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

Em seguida, acesse a URL [http://127.0.0.1:8000/teste/](http://127.0.0.1:8000/teste/`).

### Passando Parâmetros para o Template do Django

Agora, iremos ver como podemos passar alguns parâmetros do Python para o template HTML utilizando tags do Django (através da biblioteca [Jinja](https://jinja.palletsprojects.com/en/3.1.x/)).

Em seguida, edite o arquivo `views.py` na pasta `myapp` e coloque o seguinte conteúdo:

```python
from django.http import HttpResponse
from django.template import loader

def teste(request):
    template = loader.get_template('paginateste.html')
    context = {
        "nome": "José Silva",
        "idade": 30,
        "email": "jose.silva@email.com",
        "telefone": "3333-1234"
    }
    return HttpResponse(template.render(context, request))
```

Em seguida, edite o arquivo HTML com nome `paginateste.html` na pasta `templates` com o seguinte conteúdo:

```html
<!DOCTYPE html>
<html>
<body>

<h1>Django: Tags de Templates</h1>

<p>Neste exemplos utilizamos as tags de templates do Django (Jinja)</p>

<ul>
    <li><b>Nome:</b> {{ nome }} </li>
    <li><b>Idade:</b> {{ idade }} </li>
    <li><b>E-mail:</b> {{ email }} </li>
    <li><b>Telefone:</b> {{ telefone }} </li>
</ul>

</body>
</html>
```

Em seguida, execute o projeto django:

```bash
python3 manage.py runserver
```

Em seguida, acesse a URL [http://127.0.0.1:8000/teste/](http://127.0.0.1:8000/teste/`).

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

OBS: Quando criamos o projeto Django, obtivemos um banco de dados SQLite vazio. Ele estava na raiz da pasta `aula-django-01` e possui o nome de arquivo `db.sqlite3`. Por padrão, todos os modelos criados no projeto Django serão criados como tabelas neste banco de dados.

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

Agora reinicie o servidor:

```bash
python3 manage.py runserver
```

Na janela do navegador, digite na barra de endereço [127.0.0.1:8000/admin/](127.0.0.1:8000/admin/)

Preencha o formulário com o nome de usuário e senha corretos (`admin` e `admin`):

Na tela aberta você pode criar, ler, atualizar e excluir grupos e usuários, mas onde está o modelo de Livro?

O modelo Livro está faltando, como deveria estar. Você tem que informar ao Django quais modelos devem estar visíveis na interface administrativa.

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

Agora volte para o navegador e atualize a barra de endereço [127.0.0.1:8000/admin/](127.0.0.1:8000/admin/)

Clique em Livros faça a inserção de alguns livros no modelo criado.

### Visualizando o Modelo de Dados

Existem diversas ferramentas que podem ser utilizadas para ver o banco de dados do modelo criado. Uma dessas ferramentas é o [site SQLite Online](https://sqliteonline.com/). Acesse esse site e carregue o banco de dados chamado `db.sqlite3` localizado na raiz do projeto.

Execute o comando abaixo nessa ferramenta para listar os livros que você cadastrou utilizando o ambiente administrativo.

```sql
SELECT * FROM myapp_livro;
```

### Fim do Tutorial

Chegamos ao final desta aula/tutorial. É importante entender o que faz cada um dos comandos acima explicados. Caso tenha dúvidas acesse o site da documentação do Django e/ou o curso de Django da w3schools nos links abaixo.

* [Documentação Django](https://docs.djangoproject.com/pt-br/5.0/)
* [Curso Django w3schools](https://www.w3schools.com/django/index.php)
