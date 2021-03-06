## Blog API
- Добавление статьи (Можно чисто номинально, как сущность, к которой крепятся комментарии).
- Добавление комментария к статье.
- Добавление коментария в ответ на другой комментарий (возможна любая вложенность).
- Получение всех комментариев к статье вплоть до 3 уровня вложенности.
- Получение всех вложенных комментариев для комментария 3 уровня.
- По ответу API комментариев можно воссоздать древовидную структуру.

### Install docker
<pre><code>
sudo apt update
sudo apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
sudo apt update
sudo apt install docker-ce
</code></pre>
 
### Install Docker Compose  
for linux 
<pre><code>sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose</code></pre> 
<pre><code>sudo chmod +x /usr/local/bin/docker-compose</code></pre>
for other os: https://docs.docker.com/compose/install/  

### Run project
<p>Сredetionals in the .env file.
If you have another base in postgres - change them.<br>
PostgreSQL with postgres database is used by default.</p>  
<pre><code>sudo docker-compose up</code></pre>

### Blog API
http://localhost:8000/api/

### Documetnation API
http://localhost:8000/redoc/

### Django administration
http://localhost:8000/admin/  
Create superuser 
<pre><code>docker exec -it myblog_web_1 python manage.py createsuperuser</code></pre>
