# Currency-Converter-App
Real Time Currency Converter Web Application with Python Flask
the web server calculate the rate of the currency with comparitive with another currecny.

# Auti url
to see all the history

## Common setup
Clone the repo and install the dependencies.
```bash
git clone https://github.com/aishyawawdi/Currency-Converter.git
```

## RUN By Flask

open cmd and get into the file location and then enter:
```bash
py -m pip install -r requirements.txt
set FLASK_APP=front-end.py
flask run
```
go the the url: https://127.0.0.0:5000) (port=5000)

## RUN By Docker

open cmd and get into the file location and then enter:
```bash
docker build -t frontend .
```
after getting the image now we can run the container:
```bash
docker run -d -p 5000:5000 frontend
```
go the the url: https://127.0.0.0:5000) (port=5000)

## RUN By kubernetes:  
```bash
git clone https://github.com/aishyawawdi/Currency-Converter.git
cd Currency-Converter.git
cd Kubernetes 
kubectl apply -f backend_deployment.yml -f backend_service.yml -f frontend_deployment.yml -f frontend_service.yml -f auti_deployment.yml -f auti_service.yml  

```
go to the url: "127.0.0.1:30039"

## RUN By Terraform:  
```bash
git clone https://github.com/aishyawawdi/Currency-Converter.git 
cd Currency-Converter.git 
```
go to main.tf file and change the key name your Keypair name in your aws   
add your privte key file to the folder
set your access_key and secret_key of aws instead of ********

then run:
terraform init 
terraform apply

in the last when finish:
terraform destroy
  
then go to your aws console and get your instance public ip run through "your-instance-ip:7000"  


