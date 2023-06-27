# WACAD012-Conteineres



1. PRECISA TER INSTALADO DOCKER E DOCKER COMPOSE
   - Docker: https://docs.docker.com/get-docker/
   - Docker Compose: https://docs.docker.com/compose/install/

2. Após baixar e descompactar a pasta principal "webacademy-projeto", verifique se dentro dela você possui as seguintes pastas e arquivos:
   - webacademy-livros-backend: Pasta contendo o código-fonte do backend.
   - webacademy-livros-frontend: Pasta contendo o código-fonte do frontend.
   - docker-compose.yml
   - init.sql

3. Abra o terminal e navegue até o diretório raiz "webacademy-projeto" utilizando o comando `cd`. Por exemplo:
   ```
   cd /caminho/para/webacademy-projeto
   ```

4. Dentro do diretório raiz, você também encontrará o arquivo `docker-compose.yml` que define as configurações do Docker Compose para o seu projeto.

5. Abra o arquivo `docker-compose.yml` em um editor de texto e verifique as configurações, como as portas utilizadas pelos serviços. Certifique-se de que essas portas não estejam em conflito com outros serviços em execução em sua máquina.

6. No terminal, execute o seguinte comando para iniciar os contêineres do seu projeto:
   ```
   docker-compose up
   ```
   Os contêineres serão construídos e iniciados com base nas configurações definidas no arquivo `docker-compose.yml`. Neste momento, as pastas `mysql-data` e `log` serão criadas automaticamente.

   Se preferir executar os contêineres em segundo plano, utilize o seguinte comando:
   ```
   docker-compose up -d
   ```
   Dessa forma, os contêineres serão iniciados em segundo plano.

7. Aguarde até que todos os contêineres sejam iniciados corretamente. O Docker irá baixar as imagens e configurar os serviços conforme necessário. Isso pode levar alguns minutos, dependendo da velocidade da sua conexão com a internet.

8. Uma vez que todos os contêineres estejam em execução, você pode acessar o seu projeto através das seguintes URLs:
   - Backend: http://localhost:4444
   - Frontend: http://localhost:8000
   - phpMyAdmin: http://localhost:8080

9. Volumes
    - Na pasta raiz mysql-data terá acesso aos dados do container do mysql com todos os arquivos.
    - Na pasta raiz log terá acesso aos log do backend
     
11. Utilize essas URLs para interagir com o seu projeto. Por exemplo, você pode fazer solicitações HTTP para o backend ou visualizar o frontend no seu navegador.

12. Se você precisar parar os contêineres, abra uma nova janela do terminal, navegue até o diretório raiz do projeto e execute o seguinte comando:
    ```
    docker-compose down
    ```
    Isso irá encerrar e remover os contêineres. Os dados armazenados no volume do MySQL serão preservados nas futuras execuções do projeto.

Lembre-se de que sempre que quiser iniciar o projeto novamente, basta repetir o passo 6.

Certifique-se de ter o Docker e o Docker Compose instalados antes de iniciar o passo a passo.
