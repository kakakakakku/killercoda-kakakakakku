# Running Containers on Amazon EKS

- Lab.0「Pod を起動する」
- 20 min 程度
- kubectl コマンドを使って基本的な操作を試します

## 操作方法

>コマンドをクリックすると直接実行できます。

以下のコマンドを実行すると、Kubernetes v1.24.0 と表示されます。

`kubectl version`{{exec}}

以下のコマンドを実行すると、1台の Kubernetes ノード情報（コントロールプレーンとデータプレーン同居）を確認できます。

`kubectl get nodes`{{exec}}

以下のコマンドを実行すると、詳細なノード情報を確認できます。

`kubectl get nodes -o wide`{{exec}}
