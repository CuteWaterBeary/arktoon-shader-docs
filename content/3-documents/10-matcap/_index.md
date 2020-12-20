---
title: "MatCap"
date: 2019-02-10T17:18:45+09:00
draft: false
categories: ["", ""]
description: ""
image: ""

author: ""
weight: 100
---
### できること
メッシュに対して、予め「ライティングされた光源」（＝`MaterialCapture`,`MatCap`）となるテクスチャを設定できます  
（※作例画像/gif動画準備中）
<!-- {{< figure src="/images/cat_common1.gif" >}} -->
### 各項目について
#### Blend Mode
MatCapで決定した色を基本色にどのように合成するかを設定します
- Unused: この機能を使いません（デフォルト）
- Add: 既存の色にMatCapの色を加えます（加算）
- Lighten: 既存の色と比較し、明るい方を表示します（比較(明)）
- Screen: 既存の色と比較し、スクリーン合成します（逆乗算）
#### Blend & Mask
`Blend Mode`で設定した方法でどの程度ブレンドするかを設定します  
マスクテクスチャを使うことで、メッシュの部分ごとのブレンドの強度を制御できます
#### Texture & Color
MatCapとして着色するテクスチャ×色を指定します
#### Normal Map mix
MatCapを着色する際、`Common`や`Details`で設定した`NormalMap`をどの程度考慮するかをスライダーで指定できます
#### Shadow mix
`Shading / Shadow`カテゴリで指定した「陰」の部分に効果を反映させたくない場合、  
このスライダーを設定することで効果を抑制できます