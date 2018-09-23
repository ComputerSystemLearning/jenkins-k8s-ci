依次创建这四个yml文件，实现对jenkins应用在k8s下的部署

kubectl create -f pv-jenkins.yml

kubectl create -f pvc-jenkins.yml

kubectl create -f jenkins-statefulset.yml

kubectl create -f jenkins-service.yml
