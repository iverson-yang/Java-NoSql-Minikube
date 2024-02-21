# Java-NoSql-Minikube
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
   3. Deploy MongoDB in Minikube  
      ```
      kubectl create deployment mongodb --image=mongo --port=27017
      kubectl expose deployment mongodb --type=NodePort --port=27017 --target-port=27017
      ```
   4. Get the external IP address of the “mongodb” Service, run following command:  
      ```
      minikube service mongodb
      ```
      Then we get external URL http://127.0.0.1: &lt;port&gt;, in my case it's http://127.0.0.1:59619
      
