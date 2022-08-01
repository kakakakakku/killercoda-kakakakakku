# Step.1

## Pod を起動する

以下のコマンドを実行します。Pod は1つもありません。

`kubectl get pods`{{exec}}

次に Pod を起動します。

```sh
wget https://master.d18una3n17zfc6.amplifyapp.com/docs/running-eks11/manifests/pod.yaml
kubectl apply -f pod.yaml
```{{exec}}

kubectl get コマンドで、STATUS が Running になるまで待ちましょう。

`kubectl get pods`{{exec}}

簡単に Pod を起動できました。

kubectl describe コマンドで、詳細な Pod 情報を確認できます。

`kubectl describe pod hello-pod`{{exec}}

kubectl delete コマンドで、一度 Pod を消しておきましょう。

`kubectl delete -f pod.yaml`{{exec}}
