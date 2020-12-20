---
title: "Rim"
date: 2019-02-10T17:18:45+09:00
draft: false
categories: ["", ""]
description: ""
image: ""

author: ""
weight: 120
---

### できること
メッシュのリム（ヘリ、枠）に対する光を指定できます（リムライトと呼ばれます）  
（※作例画像/gif動画準備中）
<!-- {{< figure src="/images/cat_common1.gif" >}} -->
### 各項目について
#### Blend Start
リム効果を開始する位置を指定します  
スライダーが高いほど、側面に寄ります
#### Blend End
リム効果が最大になる位置を指定します  
スライダーが高いほど、側面に寄ります  
`Blend Start`よりも低い値を設定すると、本来とは逆の効果が発生します
#### Power type
`Blend Start`から`Blend End`までの推移する式を選択できます
- Linear: 線形に変化します
- Pow3, Pow5: 変化位置を0～1とした数字に対して、効果をその値の3乗および5乗で計算します  
要するに変化量にイージングがかかったようになります
#### Blend & Mask
リム効果の強さとマスクテクスチャを指定します
#### Texture & Color
リム効果の色またはテクスチャを指定します
#### Use Base Color
リム効果に基本色を指定したい場合はチェックします
#### Shadow mix
`Shading / Shadow`カテゴリで指定した「陰」の部分に効果を反映させたくない場合にスライダーで指定
