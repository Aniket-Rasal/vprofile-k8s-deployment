<<<<<<< HEAD
# Prerequisites
#
- JDK 17 or 21
- Maven 3.9
- MySQL 8

# Technologies 
- Spring MVC
- Spring Security
- Spring Data JPA
- Maven
- JSP
- Tomcat
- MySQL
- Memcached
- Rabbitmq
- ElasticSearch
# Database
Here,we used Mysql DB 
sql dump file:
- /src/main/resources/db_backup.sql
- db_backup.sql file is a mysql dump file.we have to import this dump to mysql db server
- > mysql -u <user_name> -p accounts < db_backup.sql


=======
vProfile Kubernetes Deployment
📌 Overview

Deployed a multi-tier microservices application (vProfile) on Kubernetes with full integration of database, messaging, and caching layers.

🛠️ Tech Stack
Kubernetes
Docker / containerd
MySQL
RabbitMQ
Memcached
Apache Tomcat
Maven
⚙️ Architecture

Client → NodePort / Ingress → Tomcat → MySQL / RabbitMQ / Memcached

🚀 Deployment
Build Application
mvn clean package
Build Docker Image
docker build -t vprofile-app .
Load Image into Cluster
docker save vprofile-app > vprofile.tar
sudo ctr -n k8s.io images import vprofile.tar
Deploy to Kubernetes
kubectl apply -f k8s/
🌐 Access Application
http://<NODE-IP>:<NODEPORT>
🔐 Login
Username: admin_vp
Password: admin_vp
🧪 Key Learnings
Fixed Java version mismatch (JDK 11 vs 17)
Resolved javax vs jakarta compatibility issues
Debugged MySQL connectivity & schema setup
Fixed RabbitMQ authentication issues
Understood config flow (source → image → pod)
📊 Outcome

Application successfully deployed and accessible via browser.

👨‍💻 Author

Aniket Rasal
=========================
>>>>>>> 48320334878bb83569fbbb45c57713e59de6bd90
