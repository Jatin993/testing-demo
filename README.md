# testing-demo
### 2.Create docker-compose file which includes below services 
#     :nginx (port 80 and 443 should assign)
#     :MySQL (pre-defined root user password)
#     :PHP   (should have all php extensions)
#     :redis-server

cd /home/ubuntu/wordpress

cd docker-compose-php-nginx-mysql-redix/

Run This Command in Terminal
docker-compose up -d

open this link in web browser: http://65.2.162.53/

docker-compose down

cd ..



## 3. Configure any monitoring tool on to the server and create "container monitoring dashboard"
##For Monitoring we can Use this

docker volume create portainer_data

docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:2.16.2



### 5. Deploy any Php website (E.g. basic wordpress / drupal site) with the use of docker (Use nginx, mysql, php services) 
### 7. Configure ssl for the domain
### 8. Site should redirect forcefully from http to https
### 9. Provide ssh access of server and create a README file 
cd deploy-any-php-website

docker-compose up -d

docker-compose up -d --force-recreate --no-deps webserver

open this link in web browser
https://nginx.brahmanienterprise.tk/

docker-compose down
