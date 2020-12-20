---
title: "Reflection"
date: 2019-02-10T17:18:45+09:00
draft: false
categories: ["", ""]
description: ""
image: ""

author: ""
weight: 110
---

### できること
メッシュに対して鏡面反射を設定します。  
（※作例画像/gif動画準備中）
<!-- {{< figure src="/images/cat_common1.gif" >}} -->
### 各項目について
#### Use Reflection Probe
シーン中のReflection Probeを使用する場合はチェックします  
チェック無し、またはチェックがあってもシーンに存在しない場合はCubemapが使用されます  
#### Smoothness & Mask
面の「つやつや度」を設定します。高いほど光が集まり、強く反射します  
Maskを指定することでメッシュの部分部分で設定が可能です  
#### Cubemap（Fallback）
反射もととなるCubemapテクスチャを設定します  
Use Reflection Probeがオンの場合は、シーンに存在しない場合に自動的に設定されます  
#### Normal Map mix
リフレクションに対してNormalMapをどの程度考慮するかをスライダーで設定します
#### Shadow mix
陰影部分にどの程度Reflectionを適用”しない”かをスライダーで指定します
#### Suppress Base Color
Reflectionの着色に応じてメッシュ基本色を隠す強さをスライダーで設定します
