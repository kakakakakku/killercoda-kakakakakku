# Step.2

## Deployment を起動する

以下のコマンドを実行します。default Namespace と Kubernetes 関連の Namespace があります。

`kubectl get namespaces`{{exec}}

次に eks-course Namespace を追加します。

```sh
wget https://master.d18una3n17zfc6.amplifyapp.com/docs/running-eks11/manifests/namespace.yaml
kubectl apply -f namespace.yaml
kubectl get namespaces
```{{exec}}

次に eks-course Namespace に Deployment を起動します。

```sh
wget https://master.d18una3n17zfc6.amplifyapp.com/docs/running-eks11/manifests/deployment.yaml
kubectl apply -f deployment.yaml
```{{exec}}

自動的に Deployment 1つ / ReplicaSet 1つ / Pod 3つが起動しています。-n オプションを使って Namespace を指定しています。

```sh
kubectl get deployments -n eks-course
kubectl get replicasets -n eks-course
kubectl get pods -n eks-course
```{{exec}}

しかし Namespace を指定しているため、default Namespace に Pod は起動していません。

`kubectl get pods`{{exec}}

Pod 1つ、停止してみましょう。xxxxxxxxxx-yyyyy の部分はコマンド結果を確認して置き換えます。

`kubectl delete pod hello-deployment-xxxxxxxxxx-yyyyy -n eks-course`{{exec}}

もう一度 Pod を確認すると、1つだけ AGE が新しくなっているはずです。

`kubectl get pods -n eks-course`{{exec}}
