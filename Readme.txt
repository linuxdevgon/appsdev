   Using docker-compose 

  Clone this repository, then start services locally using Docker Compose:
1.docker-compose build
2.docer-compose up
3.Opening the localhost on port 8000 should open our output

   Run with Docker

1.Build the image with
sudo docker build -t pythonapp .
2.Run the container with
sudo docker run -d -p 8000:8000  --name hello-app pythonapp
3.Go to localhost:8000. You should see "Hello, World!It's works"

   Deploy to Heroku

1.change in file Dockerfile CMD part of section "0.0.0.0:8000" to "0.0.0.0:$PORT"
2.You must have an account on www.heroku.com
3.In your CLI type next command:
4.heroku container:login
5.heroku create $nameyourapp
6.heroku container:push web --app $nameyourapp
7.heroku container:release web --app $nameyourapp
8.heroku ps:scale web=1 --app $nameyourapp
9.heroku open --app $nameyourapp
In your brother you will see "Hello, World!It's works"