依次创建这四个yml文件，实现对jenkins应用在k8s下的部署

1. kubectl create -f pv-jenkins.yml

2. kubectl create -f pvc-jenkins.yml

3. kubectl create -f jenkins-statefulset.yml

4. kubectl create -f jenkins-service.yml
