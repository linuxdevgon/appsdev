#Flask-Docker-Heroku
####Using docker-compose
Clone this repository, then start services locally using Docker Compose
#####In your CLI RUN next command:
```
 docker-compose build
 docer-compose up
    ```
Opening the localhost on port 8000 should open our output

#### Run with Docker
1.Build the image with
```
docker build -t pythonapp .
    ```
2.Run the container with
```
docker run -d -p 8000:8000  --name hello-app pythonapp
    ```
3.Go to localhost:8000. You should see "Hello, World!  It 's works"

#### Deploy to Heroku
   1.Change in file Dockerfile CMD part of section "0.0.0.0:8000" to "0.0.0.0:$PORT"
   2.You must have an account on www.heroku.com
   3.In your CLI type next command:
```
heroku container:login
heroku create $nameyourapp
heroku container:push web --app $nameyourapp
heroku container:release web --app $nameyourapp
heroku ps:scale web=1 --app $nameyourapp
heroku open --app $nameyourapp
    ```
In your brother you will see "Hello, World!It's works"
