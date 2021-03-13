docker-compose run .

Create registry

docker run -d -p 5000:5000 --restart always --name registry registry:2

docker build -t maceta:1 .

docker tag maceta:1 localhost:5000/maceta:1

docker push localhost:5000/maceta:1

docker pull localhost:5000/maceta:1

Modificamos el docker-compose para que coja la imagen que hemos subido al registry

Create Jenkins, gog and registry
docker-compose -f docker-compose.yml up --build
