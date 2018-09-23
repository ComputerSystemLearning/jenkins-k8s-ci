kubectl create -f pv-jenkins.yml

kubectl create -f pvc-jenkins.yml

kubectl create -f jenkins-statefulset.yml

kubectl create -f jenkins-service.yml
