---
title: "半透明の表現例"
date: 2019-02-11T11:33:07+09:00
draft: false
categories: ["", ""]
description: "メッシュに半透明な部分がある場合の設定例"
image: ""

author: ""
weight: 3
---
### 半透明のあるメッシュの表現の例
動画５（メッシュの一部に半透明なところがある）
1. シェーダーを `Fade` のつくものに変更
2. `Common/Main Texture`にアルファ情報のあるテクスチャを設定するか、  
色設定ダイアログでアルファ値を変更する

{{% notice info %}}
半透明に設定したメッシュを重ねた場合、予期しない描画結果を招く場合があります。`fade`を使ったマテリアルは最低限とし、可能な限り`AlphaCutout`または`Opaque`の利用を推奨します。
{{% /notice %}}