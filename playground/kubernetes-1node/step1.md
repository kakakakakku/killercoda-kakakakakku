# step1

ノードを確認します。

`kubectl get nodes`{{exec}}

nginx Pod を起動します。

`kubectl run nginx --image nginx:1.21`{{exec}}

Pod を確認します。

`kubectl get pods`{{exec}}
