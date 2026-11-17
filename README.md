# E-commerce DevOps Project

Java (Servlet + JSP) web app built with Maven into `ecommerce.war` and deployed to Tomcat 9.

Pipeline: GitHub -> Jenkins -> Ansible -> Tomcat / Docker -> Kubernetes

## Build
```
mvn clean package        # creates target/ecommerce.war
```

## Run on Tomcat 9
Copy `target/ecommerce.war` to Tomcat's `webapps/` folder, then open:
- http://<server-ip>:8080/ecommerce/
- http://<server-ip>:8080/ecommerce/shop

## Docker
```
cp target/ecommerce.war .
docker build -t <dockerhub-user>/ecommerce:latest .
docker run -p 8080:8080 <dockerhub-user>/ecommerce:latest
```
