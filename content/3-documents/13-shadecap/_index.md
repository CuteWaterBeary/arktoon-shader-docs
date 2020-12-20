---
title: "Shade Cap"
date: 2019-02-10T17:18:45+09:00
draft: false
categories: ["", ""]
description: ""
image: ""

author: ""
weight: 130
---

### できること
メッシュに対して、予め「ライティングされた陰」テクスチャを設定できます  
MatCapの暗い版です。造語です。  
（※作例画像/gif動画準備中）
{{% notice info %}}
近いうちに「Light Shutter」モードをShadingカテゴリに移動して、他の機能を削除する気がします。
{{% /notice %}}
<!-- {{< figure src="/images/cat_common1.gif" >}} -->
### 各項目について
#### Blend Mode
ShadeCapで決定した色をどのように混ぜるかを指定します
- Unused: この機能を使いません（デフォルト） 
- Darken: 既存の色と比較し、暗い方を表示します（比較(暗)）
- Multiply: 既存の色と乗算します
- Light Shutter: 決定した色を「ライティングの受光方向のマスク」とみなして陰を設定します  
つまり、黒いテクスチャを指定すると、メッシュ全体が陰に入ったようになります
#### Blend & Mask
`Blend Mode`で設定した方法でどの程度ブレンドするかを設定します  
マスクテクスチャを使うことで、メッシュの部分ごとのブレンドの強度を制御できます
#### Texture & Color
ShadeCapとして着色するテクスチャ×色を指定します  
`Light Shutter`を使う場合、白黒テクスチャでない場合に予期しない挙動になるかもしれません
#### Normal Map mix
ShadeCapを着色する際、`Common`や`Details`で設定した`NormalMap`をどの程度考慮するかをスライダーで指定できます