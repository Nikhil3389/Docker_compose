# Docker_compose

Steps to perfrom docker compose
1.  Installing Docker Compose

sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose
docker-compose --version

2.  Setting Up a docker-compose.yml File

mkdir ~/compose-demo
cd ~/compose-demo

mkdir app
nano app/index.html
Place the following content into this file:
<!doctype html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <title>Docker Compose Demo</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/kognise/water.css@latest/dist/dark.min.css">
</head>
<body>

    <h1>Nikhil Kumar Kataria</h1>
    <p>Here is my Reg. No 12001995</p>

</body>
</html>



![image](https://user-images.githubusercontent.com/71307854/228984866-f8f25b4a-b73b-47c4-9fc9-f037d0691b50.png)

nano docker-compose.yml

version: '2.6'
services:
  web:
    image: nginx:alpine
    ports:
      - "8000:80"
    volumes:
      - ./app:/usr/share/nginx/html

![image](https://user-images.githubusercontent.com/71307854/228985028-c569447e-b6ba-4022-b199-2e9b84adae2a.png)

3. Running Docker Compose
sudo docker-compose up -d

 sudo docker-compose ps

![image](https://user-images.githubusercontent.com/71307854/228985212-508b37fe-4e89-4094-8d3e-3ba426354640.png)


![image](https://user-images.githubusercontent.com/71307854/228985295-b60de665-219e-4f2a-8f43-353d35687425.png)

