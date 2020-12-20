---
title: "Parallaxed Emission"
date: 2019-02-10T17:18:45+09:00
draft: false
categories: ["", ""]
description: ""
image: ""

author: ""
weight: 150
---
### できること
視差のあるEmissionテクスチャを貼り付けることができます  
（※作例画像/gif動画準備中）
<!-- {{< figure src="/images/cat_common1.gif" >}} -->
### 各項目について
#### Texture & Color
表示させたいテクスチャと色を指定します
#### TexCol Mask
Parallaxed Emissionを適用する場所を、マスクテクスチャで指定します
#### Parallax Depth & Mask
視差の深度を設定します  
正の値だと手前にくるようになり、負の値だと奥に行ったような表現になります  
マスクテクスチャを指定することで、深度に乗算し、メッシュの部分ごとに深度を調節できます
##### Invert Depth Mask
マスクテクスチャの効果を逆に設定します
