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
    - cd Cadastro_Leads_Proj
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
[X] Registrar o app cadastro_leads
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
[X]   Criar a view para a rota inicial
o	Dentro da pasta cadasttro_leads (app) abrir o arquivo views.py
•	    from django.shortcuts import render
•	    from django.http import HttpResponse
•	
•	    def index(request):
        return HttpResponse("<h1>Seja bem vindo</h1>")

[X]  Registrar a rota inicial
o	Dentro da pasta Cadastro_leadsProj(app) abrir o arquivo urls.py
•	from django.contrib import admin
•	from django.urls import path, include
•	
•	urlpatterns = [
•	    path('admin/', admin.site.urls),
•	    path('',include('Cadastro_leads.urls')),

[X]  Criar o arquivo index.html
o	  Dentro da pasta cadastro_leads(app), crie a pasta templates
o	Dentro da pasta templatescrie seus arquivos HTML começando pelo index.html
o	No arquivo views.py que está dentro da pasta do app faça a seguinte alteração de código:
•	from django.shortcuts import render
•	
•	def index(request):
    return render(request,'index.html')

[]  Integrar arquivos estáticos (CSS, JS, IMG)
o	Dentro da pasta do projeto (Cadastro_leads_Proj), criar a pasta static
o	Dentro da pasta static, colocar as imagens, os arquivos css e os arquivos js que for utilizar
o	No arquivo settings.py:
	realize a importação da biblioteca os através do comando import os
	na linha ~58 adicione o caminho dos templates da seguinte forma:
'DIRS': [os.path.join(BASE_DIR, 'cadastro_leads/templates')],
	no final do arquivo, após a linha STATIC_URL insira o seguinte código:

