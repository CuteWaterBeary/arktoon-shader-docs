---
title: "Emissive Freak"
date: 2019-02-10T17:18:45+09:00
draft: false
categories: ["", ""]
description: ""
image: ""

author: ""
weight: 160
---
### できること
アニメーション付きのEmissionテクスチャを2枚まで使用できる、特殊カテゴリです
（※作例画像/gif動画準備中）
<!-- {{< figure src="/images/cat_common1.gif" >}} -->
### 各項目について
#### Texture & Color
発行させたいテクスチャと色を指定します
#### TexCol Mask
テクスチャと色にマスクをしたい場合にマスクを指定します  
マスクテクスチャは後述のアニメーションでは動きません
#### Scroll U
U方向のテクスチャスクロール速度を設定します
#### Scroll V
V方向のテクスチャスクロール速度を設定します
#### Depth & Mask
視差効果を使う場合、その深度とマスクを設定します
##### Invert Depth Mask
深度マスクを逆に設定する場合はチェックします
#### Breathing & Mix
`Texture & Color`の色に対して、じわっと浮かび上がり、じわっと消えるアニメーション設定します（ブリージング効果）
#### Blink Out & Mix
`Texture & Color`の色に対して、突然浮かび、じわっと消えるアニメーションを設定します
#### Blink In & Mix
`Texture & Color`の色に対して、じわっと浮かび、突然消えるアニメーションを設定します
#### Hue Shift & Mix
`Texture & Color`の色に対して、色相変更アニメーションを設定します