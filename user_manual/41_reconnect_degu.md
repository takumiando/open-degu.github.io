---
layout: default
title: Deguの再接続
parent: ユーザーマニュアル
nav_order: 41
---

# Deguの再接続

Deguを改めて接続し直したり、別のDeguゲートウェイに接続する方法を説明します。

## DeguをAWS IoT Coreから削除する

AWS IoT Coreに登録されているDeguを削除してください。削除するには、登録されているモノのページで、`アクション`->`削除` をクリックしてください。

![](images/delete_thing.png)

## Deguの接続情報を消去する

Deguに書き込まれている、Threadの接続情報(OpenThread Network Information領域)を消去します。

DeguをLinux PCに接続したとき、'/dev/sdx'としてUSB Mass Storage領域にアクセスできる場合、次のコマンドでこの領域を消去してください。

```
$ sudo dd if=/dev/zero of=/dev/sdx bs=1k count=16 seek=16
```

## DeguをDeguゲートウェイへ再接続する

これで、DeguをDeguゲートウェイに接続する前の状態に戻すことができました。再度、[Deguを登録・接続](40_connect_degu.md)してください。
