## jenkins的k8s部署及应用
### 一. 环境
    1.CI/CD集群下部署应用
    2.jenkins镜像为 jenkinsci/jenkins (docker search jenkins可以找到所需镜像)
### 二. 部署 Jenkins
####    1 . 按照以下顺序分别创建这四个文件：
        1).    pv-jenkins.yml
        2).    pvc-jenkins.yml
        3).    jenkins-statefulset.yml
        4).    jenkins-service.yml
    其中文件内容所在的地址为：https://github.com/penpenpenpen/jenkins-k8s-ci
####    2 . 设置jenkins
   1). 获取外部访问jenkins的端口(这里为30085)，ip为CI/CD集群下的任意节点ip，这里选用10.151.33.87
 <div style="text-align: center">
 <img src="picture/1.png"/>
 </div>
   2). 按照jenkins界面的提示逐步操作，得到下面界面
 <div style="text-align: center">
 <img src="picture/2.png"/>
 </div>
   3). 点击 “系统管理” —> “管理插件” —> “可选插件” —> “Kubernetes ” 勾选安装
 <div style="text-align: center">
 <img src="picture/3.png"/>
 </div>
  4).  点击 “系统管理” —> “系统设置” —> “新增一个云” —> 选择 “Kubernetes”，然后填写 Kubernetes 和 Jenkins 配置信息     
  (其中Jenkins地址的ip为CLUSTER-IP(这里为172.29.32.50)，端口为8080，Kubernetes地址的ip为10.151.33.87，端口为8080） 
 <div style="text-align: center">
 <img src="picture/4.png"/>
 </div>
