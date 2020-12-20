---
title: "Details"
date: 2019-02-10T17:18:45+09:00
draft: false
categories: ["", ""]
description: ""
image: ""

author: ""
weight: 70
---
### できること
`Common`および`Shading`（Custom color Shading利用中）で決定された色に対して、  
オーバーレイで追加のテクスチャを指定します。  
基本的には[StandardシェーダーのDetail Maps](https://docs.unity3d.com/ja/2018.4/Manual/StandardShaderMaterialParameterDetail.html)と同じ使用方法を想定しています。  
（※作例画像/gif動画準備中）

<!-- {{< figure src="/images/cat_common1.gif" >}} -->
### 各項目について
#### Mask
後述の各種テクスチャを限定的に適用したい場合、Maskテクスチャを設定します
#### Detail Map & Detail Map (when shaded)
適用したい詳細テクスチャを設定し、スライダーでその強度を設定できます  
`Shading / Shadow`の`Custom color shading`でテクスチャを使っている場合、  
`Detail Map (when shaded)`にも同じテクスチャを適用するか、陰用の別の詳細テクスチャを適用できます  
#### Normal Map
適用したい詳細NormalMapを設定し、スライダーでその強度を設定できます
