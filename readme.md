<h1 align="center">
  API com autenticação  de usuário 
</h1>

<h3 align="center">
  Api Rest com Django Framework baseada no livro: 
  <a href="https://readthedocs.org/projects/djangoapibook/downloads/pdf/latest/">Building APIS</a>
</h3>

<p align="center">
  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/Bonizario/proffy?color=6842C2">

  <img alt="Repository size" src="https://img.shields.io/github/repo-size/bonizario/proffy?color=774DD6">


  <a href="https://github.com/Bonizario/proffy/blob/master/LICENSE">
    <img alt="License" src="https://img.shields.io/github/license/bonizario/proffy?color=04D361">
  </a>

  <a href="https://github.com/Bonizario/proffy/stargazers">
    <img alt="Stargazers" src="https://img.shields.io/github/stars/bonizario/proffy?style=social">
  </a>
</p>

<br />

## :pencil: Instalação da aplicação 

Para instalação é necessário ter o python na máquina.
#### :cherry_blossom: Front End
  ``` bash
$ python3 - m venv myvenv
$ pip install Django
$ pip install djangorestframework
$ django-admin startproject pollsapi
$ python manage.py migrate
$ python manage.py startapp polls

```


## 💻 API Endpoints


- **endpoint:** `/users/register/`
- **method:** `POST`
- **params:** 
```json
{
	"username": "carca",
	"password": "carcassonne"
}
```

- Em INSTALLED_APPS adicionar
- 'rest_framework','polls',
- Notique ao Django que houve mudanças no models(novos modelos criados e as mudanças devem ser aplicadas as migrações)

- > python manage.py makemigrations polls
- > python manage.py migrate

- Crie o arquivo urls.py em polls urls
- Inclua o caminho em urls.py em pollsapi
- Registre os models em admin
- Por equanto a api terá doia endpoints retornado o JSON format : /polls /polls/<id>/

- Crie um super usuário

- > python manage.py createsuperuser
- Serializers permitem que os dados instâncias do modelo e querysets sejam convertidos em dados nativos do python para serem facilmente renderizados em Json

- Acesso ao shell

- > python manage.py shell

Em header 
Authorization: Token <your token>

- **endpoint:** /users/
- **method:** POST 
```json
{
"username": "Carl",
"email": "Carl@gmail.com",
"password": "Carl123"
}
```
Header: Content-Type application/json
- **endpoint:** /login/
- **method:** POST 
```json
{
"username": "Carl",
"password": "Carl123"
}
```
return token

Header: Content-Type application/json
- **endpoint:** /polls/
- **method:** GET

Authorization Token 22555

- **endpoint:** /polls/
- **method:** POST

Header: Content-Type application/json
Authorization Token 22555
```json
{
"question": "Flask",
"created_by": "7"
}
```
- **endpoint:** polls/<id>/
- **method:** GET 

Authorization Token 22555


- **endpoint:**  polls/<id>/choices/
- **method:** POST

```json
{
"choice_text": "Aqui",
"poll": '7'
}
```
Header: Content-Type application/json
Authorization Token 22555

- **endpoint:** polls/<id>/
 - **method:** DELETE

Authorization Token 22555
