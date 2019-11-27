# prometheus_grafana
## 部署
```bash
# clone the project
git clone https://github.com/kubesys/prometheus_grafana.git

# enter the project directory
cd prometheus_grafana

# create namespace
kubectl apply -f namespace.yaml

# label node
kubectl label node [nodeName] type=monitor

# deploy node-exporter
kubectl apply -f node-exporter.yaml

# deploy prometheus
kubectl apply -f prometheus.yaml

# deploy grafana
kubectl apply -f grafana.yaml

# check status, current namespace is cloudplus
kubectl get pod -n cloudplus
```      
## 访问
visit prometheus   
http://localhost:31001

visit grafana   
http://localhost:31000

config grafana  
[official documention](https://grafana.com/docs/guides/getting_started/)

(配置dashboard使用根目录下的Cluster Monitoring.json)
