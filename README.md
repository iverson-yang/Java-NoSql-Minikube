﻿# Java-NoSql-Minikube
Env: Windows 10 Pro

1. Install minikube and docker desktop  
2. Start minikube in PowerShell  
   ```
   minikube start --driver=docker
   ```
   
3. Deploy NoSql into Minikube
   + **Mongo**  
       
   1. Pull mongo image in PowerShell  
      ```
      docker pull mongo
      ```
   2. Load mongo into Minikube env.  
      ```
      minikube image load mongo
      ```
