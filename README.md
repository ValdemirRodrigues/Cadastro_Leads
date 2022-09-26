# Cadastro Leads 
Treinando conhecimento

Pagina de cadastro de clientes

---
##  Lissta de Atividades 

Segue a lista de tarefas a serem desenvolvidas no projeto:
[X]  Pré-requisitos
[X]  Instalar o Python
[X]  Instalar Visual Studio Code
[X]  Criar e ativar o ambiente virtual
python -m venv .\venv\
venv\Scripts\activate
# se der erro no powershell utilize o comando abaixo para resolver a permissão
# Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser

Instalar o Django
python -m pip install django==3.2
[X]	 Criar o projeto PersonalCheff
```python
```django-admin.py startproject Cadastro_Leads_Proj```
[X]  Subir o servidor e testar o projeto
[X]entrar na pasta do projeto
    - cd PersonalCheffProj
[X]  Executar o projeto no servidor
```python 
`python manage.py runserver`
[X]  Alterar o idioma do projeto para pt-br
    - Abrir o arquivo settings.py e na linha 106 trocar en-us para pt-br
[X]  Alterar o timezone do projeto para America/Sao_Paulo
[X]  Cadastro_Leads_proj criar o app cadastro
    - preciso estar dentro da pasta do projeto (Proj)
```python
`python manage.py startapp cadastro_leads`

```
[X] Registrar o app receitas
    - no arquivo settings.py adicionar o app cadastro_leads na lista de apps 
INSTALLED_APPS[
    ...
    'cadastro_leads',

[X]  Configurar a rota inicial(index)
 - Dentro da pasta cadastro_leads(app) criar o arquivo urls.py
o	no arquivo urls.py
o	    from django.urls import path
o	    from . import views
o	
o	    urlpatterns = [
o	        path('', views.index, name='index')
    ]
•	  Criar a view para a rota inicial
o	Dentro da pasta receitas(app) abrir o arquivo views.py
•	    from django.shortcuts import render
•	    from django.http import HttpResponse
•	
•	    def index(request):
        return HttpResponse("<h1>Seja bem vindo</h1>")
