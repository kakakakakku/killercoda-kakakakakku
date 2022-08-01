# Step.3

## Deployment を更新する

vim で deployment.yaml を開き、image の 1.21 を 1.22 に更新しましょう。

> vim でファイルを保存する場合は :wq を使います。

`vim deployment.yaml`{{exec}}

Deployment の更新を反映します。

`kubectl apply -f deployment.yaml`{{exec}}

もう一度 Deployment / ReplicaSet / Pod を確認すると、どんな変化があるでしょうか。

全ての Pod が新しくなっているはずです。

```sh
kubectl get deployments -n eks-course
kubectl get replicasets -n eks-course
kubectl get pods -n eks-course
```{{exec}}

今度は Pod の個数を更新しましょう。もう一度 vim で deployment.yaml を開き、replicas の 3 を 5 に更新しましょう。

`vim deployment.yaml`{{exec}}

Deployment の更新を反映します。

`kubectl apply -f deployment.yaml`{{exec}}

もう一度 Deployment / ReplicaSet / Pod を確認すると、どんな変化があるでしょうか。

Pod が増えているはずです。

```sh
kubectl get deployments -n eks-course
kubectl get replicasets -n eks-course
kubectl get pods -n eks-course
```{{exec}}
