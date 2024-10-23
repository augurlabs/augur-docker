# augur-docker
A Repository for simply deploying Augur in a Docker container. 

## To Run it: 
1. Install docker desktop and start it up
2. Clone this repository
3. From a command line, pull the Augur Docker Containers: 
```{eval-rst} 
docker pull augurlabs/augur-augur-db-1
docker pull augurlabs/augur-augur-1
docker pull augurlabs/augur-redis-1
docker pull augurlabs/augur-rabbitmq-1
```
4. Edit your `environment.txt` file to contain information about you and your API keys for GitHub and GitLab
5. From the root of this repository's directory on your local computer, issue this command: 
```{eval-rst} 
docker-compose --env-file ./environment.txt up --build
```
6. Watch the container come up. This will take 1-3 minutes depending on your hardware configuration. 
7. Visit http://localhost:5002 to see your Augur frontend, and start adding repositories to be collected!

Note: Postgresql data is stored locally in a directory that remains intact throughout any startup, shutdown, or cleaning of your docker environment. 
