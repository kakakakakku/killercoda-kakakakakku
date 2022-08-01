# まとめ

Lab.0 では、以下の操作を試しました。

- Pod を起動しました
- Namespace を追加しました
- Deployment を起動しました

Pod の個数を更新する方法は他にもあります。時間があれば試してみましょう。

### kubectl scale コマンドを使う方法

`kubectl scale deployment hello-deployment -n eks-course --replicas=2`{{exec}}

Pod を確認します。

`kubectl get pods -n eks-course`{{exec}}

### kubectl edit コマンドを使う方法

> vi が起動するため replicas を 1 に更新します

`kubectl edit deployment hello-deployment -n eks-course`{{exec}}

Pod を確認します。

`kubectl get pods -n eks-course`{{exec}}

---

お疲れさまでした！

SCENARIOS ボタンを押したら終了です！
