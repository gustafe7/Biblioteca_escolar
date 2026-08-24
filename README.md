# 📚 Sistema de Biblioteca (app livros) 

App Django para controle de uma biblioteca: cadastro de livros, empréstimos, devoluções e suporte. Também busca livros na internet (Open Library API) para importar direto no acervo. 

Contém apenas o app livros (models, views, admin, urls) — falta settings.py, manage.py e os templates HTML de um projeto completo. 

- O que dá para fazer 
- Ver e buscar livros do acervo 
- Buscar livros na Open Library e cadastrá-los com um clique 
- Pedir livro emprestado (gera matrícula automática pro usuário) 
- Ver histórico de empréstimos por matrícula ou CPF 
- Devolver livro (repõe o estoque) 
- Enviar mensagem de suporte 
- Gerenciar tudo pelo Django Admin 

# Estrutura de dados 

- Livro: título, autor, editora, ano, quantidade de exemplares, disponibilidade 
- Pessoa: matrícula (automática), nome, CPF, RG, endereço, e-mail, telefone 
- Empréstimo: liga uma Pessoa a um Livro, com data e status (devolvido ou não) 
- MensagemSuporte: nome, e-mail e mensagem enviados pelo formulário de contato 

# Stacks utilizadas 

- Python 
- Django 
- Django ORM 
- Django Admin 
- Django Templates 
- HTML5 
- CSS 
- SQLite 
- Requests 
- Open Library API 

# Como usar 

- Copie a pasta livros para dentro do seu projeto Django 
- Adicione 'livros' em INSTALLED_APPS 
- Inclua as rotas no urls.py principal: path('', include('livros.urls')) 
- Rode python manage.py makemigrations livros e depois python manage.py migrate 
- Adicione requests ao seu requirements.txt e instale com pip install -r requirements.txt 
