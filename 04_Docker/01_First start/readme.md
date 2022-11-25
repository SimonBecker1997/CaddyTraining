# Run Caddy in a docker container
## Lab 1
Use the docker compose.yml in this directory to start the lab. 
1. First you need to create a volume for caddy to store its data in. Run the command:
```
docker volume create --name=caddy_data
```
2. Adjust your Caddyfile and change the domain to your actual domain.
3. Then you can start it by running the following command:
```
docker-compose up
```
