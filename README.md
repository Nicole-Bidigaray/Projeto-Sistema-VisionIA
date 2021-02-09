# Projeto Sistema VISION IA

Digitar os seguintes comandos no seu terminal

1 - Instalar a venv: pip install venv

2 - Criar a venv: python -m venv venv

3 - Entrar na venv: 
    cd venv/Scripts/activate.bat (windows); 
    source venv/bin/activate (Linux e Mac)

4 - Instalar o Django: pip install django

5 - Fazer o git clone no seu terminal: 
    git clone https://github.com/Nicole-Bidigaray/Projeto-Sistema-Estacionamento.git

6 - Migrar o banco de dados: 
    python manage.py makemigrations

7 - Criar o banco de dados: 
    python manage.py migrate

9 - Criar o seu usuário admin para o back end: 
    python manage.py createsuperuser

10 - Criar e-mail e recebimento de uma nova senha por e-mail:
     Fazer o cadastro do seu usuário e senha no sistema:
      Entrar no terminal e digitar os seguintes comandos:
        python manage.py shell
        >>> from django.contrib.auth.models import User
        >>> User.objects.count()
        *vai aparecer o número 1, ou número de usuários já cadastrados
        >>> u = User.objects.first()
        >>> u.username
        ''*vai aparecer o seu nome
        >>> exit()
      Digitar o comando:
        python3 manage.py sendtestemail seunome@example.com
      tem que aparecer essa mensagem:
        Content-Type: text/plain; charset="utf-8"
        MIME-Version: 1.0
        Content-Transfer-Encoding: 7bit
        Subject: Test email from *aqui tem que aparecer o seu nome on 2020-12-15 22:17:11.803678+00:00
        From: webmaster@localhost
        To: seunome@example.com
        Date: Tue, 15 Dec 2020 22:17:11 -0000
        Message-ID: <160807063183.9576.7595140558744646348@nicole>

        If you're reading this, it was successful.
        -------------------------------------------------------------------------------
      Entrar no shell script novamente, digitando os seguintes comandos:
        python manage.py shell
        >>> from django.contrib.auth.models import User
        >>> u = User.objects.get(username='seunome')
        >>> u.email
        ''*se não tiver cadastrado o email, vai aparecer vazio
        >>> u.email = 'seunome@example.com'
        >>> u.save()
        >>> exit()

11 - pip install django-bootstrap-form

12 - pip install django-crispy forms

13 - pip install -r requirements.txt

14 - pip freeze > requirements.txt

15 - Para rodar esse projeto em sua máquina local: 
      python manage.py runserver
