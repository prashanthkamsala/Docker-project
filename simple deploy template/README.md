docker build -t model .

docker run -p 1001:80 model:latest

http://localhost:1001/isAlive

http://localhost:1001/prediction?f=0.45