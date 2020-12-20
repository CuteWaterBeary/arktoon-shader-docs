---
title: "Outline"
date: 2019-02-10T17:18:45+09:00
draft: false
categories: ["", ""]
description: ""
image: ""

author: ""
weight: 80
---
### できること
`Outline`バリエーションを使っている場合、アウトラインの太さや色をこのカテゴリから指定できます  
（※作例画像/gif動画準備中）
<!-- {{< figure src="/images/cat_common1.gif" >}} -->
### 各項目について
#### Width & Mask
アウトラインの幅を指定します  
また、マスクテクスチャを使うことで太さを部分的に制御できます
{{% notice info %}}
太さは頂点単位で決まるため、  
頂点密度の低い箇所に関してはマスクテクスチャ通りの太さの推移にならないことがあります
{{% /notice %}}
#### Cutoff Mask & Range
`AlphaCutout`系のバリエーションを使っている場合、
アウトラインを描画しない部分をマスクで指定することができます
#### Texture & Color
アウトラインの色を指定できます
#### Base & Shading Mix
アウトラインの色に、`Common`や`Shading / Shadow`で決定した色をどの程度適用するかを設定します
#### Use Color Shift
`Texture & Color`、`Base & Shading Mix`で決定した色に対してHSV変化を加えたい場合はチェックしてください